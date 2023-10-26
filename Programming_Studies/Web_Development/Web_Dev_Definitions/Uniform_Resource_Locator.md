Sources:
https://www.howtogeek.com/356563/what-is-a-url-uniform-resource-locator/
\
A [[URL]] can consist of a bunch of different parts. There’s a hostname that maps to an [[IP]] address of a specific resource on the internet and bunch of additional information that tells your browser and the server how to handle things. You can think of an [[IP_Address]] as being something like a phone number. A [[Hostname]] is like the name of a person whose phone number you want to look up. The standard called the [[Domain_Name_System]] ([[DNS]]) works in the background like a phone book, translating the more human-friendly hostnames into the [[IP_address]]es that networks use to route traffic.
\
Keeping that analogy in mind, let’s take a look at the structure of a [[URL]] and how it works to get you where you want to go.
\
![[Pasted image 20220625213302.png]]
\
A lot of people think of a [[URL]] as just a web address, but it’s not quite that simple. A web address is a [[URL]], but all [[URL]]s are not web addresses.
\
Other services you can access on the internet—like [[FTP]]—or even locally—like MAILTO—are also URLs. The scheme portion of a [[URL]] (those letters followed by a colon) denote the protocol with which an app (like your web browser) and the server should communicate.
\
Web addresses are the most common [[URL]], but there are others. So, you might see schemes like:
\
-   [[Hypertext_Transfer_Protocol]] ([[HTTP]]): This is the underlying protocol of the web and determines what actions web servers and browsers should take in response to certain commands.
-   [[HTTP_Secure]] or [[HTTPS]]: This is a form of [[HTTP]] that works over a secure, encrypted layer for safer transport of information.
-   [[File_Transfer_Protocol]] ([[FTP]]): This protocol is often still used for transferring files over the internet.
\
In modern browsers, the scheme isn’t technically required as part of the [[URL]]. If you enter a website like “www.howtogeek.com”, your browser will automatically determine the right protocol to use. Still, some other apps (and protocols) require the use of a scheme.
\
[[Authority]]:
The [[Authority]] portion of a [[URL]] (which is preceded by two slashes) is itself broken down into a bunch of parts. Let’s start off with a very simple [[URL]]—the kind that would take you to the home page of a website.
\
![[Pasted image 20220625213841.png]]
\
In this simple example, the whole “www.example.com” part is called a [[Hostname]], and it resolves to an [[IP_Address]]. You can also type an [[IP_Address]] into your browser’s address bar instead of the [[Hostname]] if you happen to know it.
\
But, when parsing the hostname it helps to read it backward to understand what’s going on, so here are those components:
\
-   **[[Top-Level_Domain]]:** In the example here, “com” is the top-level domain. These are the highest level in the [[Domain_Name_System]] ([[DNS]]) hierarchy used to translate [[IP_Address]]es into simple language addresses that are easier for we humans to remember. These top-level domains are created and managed by the [[Internet_Corporation_for_Assigned_Names_and_Numbers]] ([[ICANN]]). The three most common top-level domains are .com, .net, and .gov. Most countries also have their own two-letter top-level domain, so you’ll see domains like .us (United States), .uk (United Kingdom), .ca (Canada), and many others. There are also some additional top-level domains (like .museum) that are sponsored and managed by private organizations. In addition to these, there are also some generic top-level domains (like .club, .life, and .news).
-   **[[Subdomain]]:** Since [[DNS]] is a hierarchical system, both the “[[WWW]]” and “example” parts of our example [[URL]] are considered [[Subdomain]]s. The “[[WWW]]” portion is a [[Subdomain]] of the “com” [[Top-Level_Domain]], and the “[[WWW]]” portion is a [[Subdomain]] of the “example” domain. That’s why you’ll often see a company with a registered name like “google.com” broken out into separate subdomains like “www.google.com,” “news.google.com,” “mail.google.com,” and so on.
\
That’s the most basic example of the authority section of a [[URL]], but things can get more complicated. There are two other components that the authority section can contain:
\
-   **User Information:** The authority section can also contain a username and password for the site you’re accessing. It’s uncommon to see this structure in URLs today, but it can happen. If present, the user info portion comes before the hostname and is followed by an @ sign. So, you might see something like “//username:password@www.example.com” if it includes the user information.
-   **Port Number:** Network devices use [[IP]] addresses to get information to the right computer on a network. When that traffic arrives, a port number tells the computer the application for which that traffic is intended. The port number is another element you won’t often see when browsing the web, but you might see it in network apps (like games) that require you to enter a [[URL]]. If the [[URL]] includes a port number, it comes after the hostname and is preceded by a colon. It would look something like this: “//www.example.com:8080.”
\
So, that’s the scheme and authority portions of a [[URL]], but as you might have guessed after looking at a lot of [[URL]]s while browsing the web, they can include even more stuff.
