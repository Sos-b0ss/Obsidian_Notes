# Basics:

- [[Public_vs_Private_IP_Addresses]]
- [[IP_Terminology]]
- [[Network_Terminology]]
- [[Network_Understanding]]
- [[Network_Functions]]
- [[Network_Topology]]
- [[Common_Protocols]]

---
## IP Addressing

You may wish to send a message to everyone on the network, in the same way you may wish to send a circular to multiple recipients, but you are also likely to want to send messages to a specific recipient. That's where addressing comes in. In IP networking this comes in the form of an IP address.

What is an IP address? You will no doubt have seen IP addresses many times. They look like this: `10.2.3.4`. So what does that represent? It actually represents four 8 bit numbers ranging from 0 (binary 00000000) to 255 (binary 11111111). This means a range of binary numbers like so:

```
0        . 0        . 0        . 0        - 255      . 255      . 255      . 255  
00000000 . 00000000 . 00000000 . 00000000 - 11111111 . 11111111 . 11111111 . 11111111
```

For a brief introduction to binary [click here](https://www.civo.com/learn/binary-introduction)

This results in a total of 4,294,967,296 IP addresses. Each address in an IP network must be unique. It is like a phone number and identifies a node on a given network.

## Subnets

You may have come across the term "subnet". Subnets are subnetworks, meaning a network divided into multiple smaller networks. Subnets can be used to separate networks logically for different purposes such as business functions like Accounts Network, Sales Network etc. They can also be divided for security and access purposes as well as many other reasons. One of the key components for dividing and identifying subnets is the "subnet mask" or "netmask".

### Subnet Masking

This may sound complicated and because of the way it is often explained with bitwise operations and binary from the start, it can seem confusing. I am going to attempt to explain the concept in a slightly different way and then explain the mechanics and notation. If we think about what we are trying to achieve more simply, all we want to do is take a network with x addresses and divide it into multiple smaller networks. Lets say we have a network consisting of only 8 addresses numbered 1 - 8. If we wanted to split this in half, we would have 2 networks of 4 addresses, the first {1, 2, 3, 4} and the second {5, 6, 7, 8} and that's fine for this very simple network and its two subnetworks. We can see fairly clearly which addresses belong to which group. But, what if we were to make this number much larger and try to subdivide it into many more networks? What if the networks weren't evenly divided? How would you identify which address belonged to which network or subnetwork? Without looking at all the addresses, how would you know where one starts and ends?

Enter the subnet mask. I am going to start the explanation of this somewhat backwards to a lot of other documentation with "CIDR notation". CIDR or Classless Inter-Domain Routing is a notation and method for dividing and allocating IP address ranges and subnets. An IP address in CIDR notation looks like this: `10.0.0.0/24` with the CIDR part being the `/24`. So what does that mean? Well it represents the 256 addresses `10.0.0.0` - `10.0.0.255`. So what about the following `10.0.0.1/24`? Well that would represent `10.0.0.1` - `10.0.1.0` right? Wrong. The range remains the same: `10.0.0.0` - `10.0.0.255`. The difference now is that we are noting a specific host address (`10.0.0.1`) within that range. Confused? Right, let's break it down.

CIDR notation allows for all 4,294,967,296 addresses to be broken down into subnet sizes of powers of 2. I.e. 2^0 = 1, 2^1 = 2, 2^2 = 4 and so on. Therefore you can't have a network with 3 addresses for example. It also somewhat prevents overlaps within evenly divided networks, so if you took the entire available range of IP addresses you could divide it into 16,777,216 `/24` subnets (4,294,967,296 / 256). Going back to our example of `10.0.0.0/24` the next available `/24` would be `10.0.1.0/24`. If we make a table, you will see a pattern:

```
10.0.0.0/24
10.0.1.0/24
10.0.2.0/24
10.0.3.0/24
10.0.4.0/24
10.0.5.0/24
10.0.6.0/24
10.0.7.0/24
10.0.8.0/24
10.0.9.0/24
10.0.10.0/24
```

Each time we are incrementing the third group of numbers separated by dots by 1. This means that each range will look as follows: `X.X.X.0` - `X.X.X.256` where `X.X.X.` remains fixed for that range. So what we are saying is that the `X.X.X.` prefix represents the range of addresses for that subnet and the final group of numbers represents individual addresses in that range. You could also look at it like this:

```
X X X   Mask
| | |
V V V
1.1.1.5 Address
      5 Host
```

Here we see that we are "masking" the first 3 parts of the address, leaving only the last. The part we mask out is known as the "network prefix" and the part we leave is known as the "host part".

What about our first example with `10.0.0.0/24`, why is that different? We'll come back to that in a moment. First, we need to get into a bit more detail about how masks work and why `/24` means what it does.

#### Bitwise Operations in Subnet Masking

If we go back to what an IP address represents when in binary form:

```
0        . 0        . 0        . 0  
00000000 . 00000000 . 00000000 . 00000000
```

We can see that it is made up of 4 groups of 8 bits. Each of these groups is also known as an "octet". An alternative to CIDR notation for masking is simply providing a subnet mask in IP notation as follows:

```
A. 10.0.0.255/24
B. Address: 10.0.0.255 Subnet Mask 255.255.255.0
```

Here both `A` and `B` represent the same information. To see what this is doing, we can convert into binary notation:

```
    11111111 . 11111111 . 11111111 . 00000000  Subnet Mask
AND 00001010 . 00000000 . 00000000 . 11111111  IP Address
---------------------------------------------
    00001010 . 00000000 . 00000000 . 00000000  Address Prefix
```

Here we see that by performing a bitwise AND on the two numbers, we get the address prefix `10.0.0.0`, thus removing the host part from the address (`X.X.X.255`).

To get the host part, we first take the one's complement of the subnet mask:

```
11111111 . 11111111 . 11111111 . 00000000  Subnet Mask
00000000 . 00000000 . 00000000 . 11111111  Subnet Mask One's Complement
```

Then the bitwise AND of the address:

```
    00000000 . 00000000 . 00000000 . 11111111  Subnet Mask One's Complement
AND 00001010 . 00000000 . 00000000 . 11111111  IP Address
---------------------------------------------
    00000000 . 00000000 . 00000000 . 11111111  Host Part
```

This gives us `0.0.0.255`.

#### Back to CIDR Notation

So how does that tie into CIDR notation? How does `255.255.255.0` represent the same thing as `/24`? Lets go back to our octets. As we know, we have 4 octets. If we multiply that out, it gives us 4 * 8 = 32 bits. Now if we take our mask in IP notation and convert it to binary:

```
11111111 . 11111111 . 11111111 . 00000000
```

We see that the first 24 bits out of 32 are used for the mask. Therefore in CIDR notation, we simply show how many bits we are using for address prefix.

## Usable Address Range

Within a subnet, not all addresses are usable. You almost always need to remove the first and last address in every subnet. This is because the first address is the network address or address prefix. In `10.0.0.0/24` that would be `10.0.0.0`. The last address is the broadcast address, in `10.0.0.0/24` that is `10.0.0.255`.

## Tools

Do you have to do this everytime you want to calculate a subnet? No, thankfully. In general, you can either memorise a table of commonly used CIDR ranges like `/24`, `/22` etc or use a tool like `sipcalc`. `sipcalc` will give you all the information you need on a given subnet like so:

```
sipcalc 10.0.0.0/24                                                                       
-[ipv4 : 10.0.0.0/24] - 0

[CIDR]
Host address            - 10.0.0.0
Host address (decimal)  - 167772160
Host address (hex)      - A000000
Network address         - 10.0.0.0
Network mask            - 255.255.255.0
Network mask (bits)     - 24
Network mask (hex)      - FFFFFF00
Broadcast address       - 10.0.0.255
Cisco wildcard          - 0.0.0.255
Addresses in network    - 256
Network range           - 10.0.0.0 - 10.0.0.255
Usable range            - 10.0.0.1 - 10.0.0.254
```