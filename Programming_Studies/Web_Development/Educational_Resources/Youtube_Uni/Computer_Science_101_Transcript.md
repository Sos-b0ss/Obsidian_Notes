What's the first thing you should do when your code throws an error? Obviously you should change nothing and try to run it again a few times.. 
\
If that doesn't work you're gonna need a computer science degree. The awesome thing about software engineering is that you can learn to code and get a high paying job, while literally having no idea how anything actually works. It all just feels like magic, like a pilot driving a giant metal tube in the sky while knowing nothing about aerodynamics or physics.
\
Welcome to computer science 101, you're about to learn the science behind the garbage code we've all been writing all this time, by learning 101 different computer science terms and concepts.
\
The Beginning:
\
Insert 'the computer', it's just a piece of tape that holds ones and zeros, along with a device that can read and write to it. It's called a [[Turing_Machine]] and in theory it can compute anything like the graphics in this video or the algorithm that recommended that you watch it.
\
At the core of modern computers we have the central processing unit ([[CPU]]). If we crack it open we find a piece of silicon that contains billions of tiny transistors which are like microscopic on off switches. The value at one of these switches is called a [[Bit]] and it is the smallest piece of information a computer can use. 
\
However one [[Bit]] by itself is not very useful so they come in a package of eight called a [[Byte]] one [[Byte]] can represent 256 different values like all the [[Character]]s that you type on your keyboard, in fact when you type into your keyboard the [[Character]] produced is actually mapped to a [[Binary]] value in a character [[Encoding]] like [[Ascii]] or utf-8, binary is just a system for counting.
\
Like the base 10 system you normally use when counting on your fingers but it only has two characters one and zero humans have a hard time reading binary so most often it's represented in a [[Hexadecimal]] base 16 format. Where ten numbers and six letters can represent a four bit group called a [[Nibble]].
\
As a developer when you write code in a programming language it will eventually be converted into [[Machine_Code]] which is a [[Binary]] format that can be decoded and executed by the [[CPU]].
\
What it doesn't do though is store data for your applications. For that computers have random access memory or [[RAM]].
\
It's like a neighborhood and inside of every house lives a [[Byte]]. Every location has a memory address which the [[CPU]] can read and write to you can think of the [[CPU]] and [[RAM]] as the brain of the computer. 
\
But in order for a computer to be useful it needs to handle input and output ([[I/O]]).
\
An input device might be the keyboard and mouse while an output device might be your monitor.
\
Luckily most developers don't need to worry about how this hardware fits together because we have operating system [[Kernel]]s like linux mac and windows that control all hardware resources via device [[Driver]].
\
Now to start hacking on the operating system. Your first entry point is the [[Shell]] which is a program that exposes the operating system to the end user.
\
It's called a [[Shell]], because it wraps the [[Kernel]]. It takes a line of text as input and produces an output this is called a [[Comman_Line_Interface]].
\
Not only can it connect to your own computer but with the secure shell protocol ([[SSH]]) it can also connect to remote computers over a network.
\
Now that you have access to the [[Mainframe]] it's time to pick a [[Programming_Language]]. 
\
Which is a tool that uses the [[Abstraction]] principle to make computers practical to work with for humans by simplifying different systems layer by layer.
\
Some languages like [[Python]] are [[Interpreted]]. That means there's a program called an interpreter that will execute each line of code one by one. Other languages like [[C+]] are [[Compiled]], they use a compiler to convert the entire program into [[Machine_Code]] in advance before the [[CPU]] attempts to execute it.
\
This results in an [[Executable]] file that can be run by the operating system without any extra dependencies.
\
Now every [[Programming_Language]] has a variety of built-in [[Data_Types]] to represent the data we're working with in our code.
\
Instead of [[Bytes]] we work with more human-friendly things like [[Character]]s and numbers. Now the most fundamental way to use data in your application is to declare a [[Variable]]. This attaches a name to a data point allowing you to reuse it somewhere else in your code.
\
[[Python]] is a [[Dynamically_Typed_Language]] which means we don't need to tell the program exactly which data type is assigned to a variable it just figures it out automatically.
\
However other languages like [[C+]] are [[Statically_Typed_Language]]s and that means you need to specify the data type of a variable in your code. When you define a variable its value is stored somewhere in memory ([[RAM]]) on the hardware and you may need to allocate and free up memory throughout the program.
\
A [[Pointer]] is a [[Variable]] whose value is the [[Memory_Address]] of another [[Variable]] which can be used for low-level memory control. 
\
Many languages don't want to deal with low-level memory management and instead implement a [[Garbage_Collector]] which automatically allocates and de-allocates memory when an object is no longer referenced in the program.
\
Now the [[Data_Type]]s available are different in every [[Programming_Language]] but typically you'll find [[Int]] to represent whole numbers which may or may not be [[Signed]] or [[Unsigned]] to represent negative numbers. As well when numbers require a decimal point they typically use the floating point type it's called a [[Float]].
\
Because there's only enough memory to represent a certain range of numbers at a certain precision and its basically used as a form of scientific notation to make computers faster.
\
If you need more range or precision many languages also have a [[Double]] that doubles the amount of memory used for the number.
\
Now when it comes to [[Character]]s you'll typically find the [[Char]] [[Data_Type]] to represent a single [[Character]] or more commonly a [[String]] to represent multiple [[Character]]s together.
\
Ultimately these [[Character]]s get stored in a [[Memory_Address]] somewhere but they need to be stored in a certain order. When the order starts with the most significant [[Byte]] and the smallest [[Memory_Address]], it's called [[Big_Endian]], or vice versa if the least significant byte is stored in the smallest address it's called [[Little_Endian]].
\
When it comes to practical software engineering one of the most fundamental things we do is organize data into data structures. The most useful data structure is probably the [[Array]] or list.
\
Just like a shopping list it organizes multiple data points in order however it also maintains an index of integers that starts at zero and goes up for every new item in the list. That can be useful but you don't actually need an index to create a list of items.
\
Another option is a [[Linked_List]], where each item has a [[Pointer]] to the next item in front of it.
\
Another option is a [[Set_Stack]] that follows the last in first out principle. It's like stacking a set of plates. Then when you want to access the data you pop the last one off the top.
\
The inverse option is a [[Queue]] which is first in first out just like when you get into the lunch line, the first person there is the first one to be fed.
\
Now another extremely useful data structure is the [[Hash]], which might also be called a map or dictionary. It's like an [[Array]] but instead of an index of integers, you define the keys that point to each individual item. This gives you a collection of key value pairs.
\
In many cases though, it's not efficient to organize data in a linear way. To address that problem we have [[Trees]], which organize [[Nodes]] together in a hierarchy that can often be traversed more quickly. This can sometimes be too rigid of a data structure though, so instead a [[Graph_Database]] can be created to connect multiple [[Nodes]] together in a virtually unlimited number of ways. A graph has a [[Node]] for the data and an [[Edge]] for the relationship between the data points.
\
Data structures are essential but they don't do anything by themselves. To do something useful you'll need to code up an [[Algorithm]], which is just code that solves a problem. I took the initiative in creating the internet in our code. We have several mechanisms for implementing [[Algorithms]], the most fundamental of which is a [[Function]], which is a block of code that takes an input then does something and [[Return]]s an output.
\
Like a [[Variable]] a [[Function]] has a name and it can be called from other parts of your code with different input parameters called [[Arguments]].
\
One thing you might do in the [[Function]] body is compare one value to another. Every language has a variety of built-in [[Operators]] like equality, greater than, and less than, that you can use to compare two values. 
\
If a is greater than b then it forms a value of true but if b is greater than a then the value is false.
\
True & false is what's known as a [[Boolean]] [[Data_Type]] and whenever your code produces a value like this it's known as an [[Expression]].
\
But not all code will produce a value, sometimes your code will simply do something which is known as a [[Statement]]. A good example is the if statement, which handles [[Conditional_Logic]].
\
For example, if the [[Condition]] is true, it will execute this code, otherwise it will short circuit and run the code inside of the else block.
\
Another very common type of [[Statement]] is a loop. A [[While_Loop]] will run this block of code over and over again until the condition in the parentheses becomes false. That can be useful, but more often than not you'll want to loop over an iterable [[Data_Type]], like an [[Array]].
\
Most languages have a [[For_Loop]] that can run some code for every object in the [[Array]] or [[Iterable]] [[Data_Structure]]s.
\
Now in some cases a [[Function]] may not have an output, which is generally called a [[Void]] [[Function]]. An interesting thing about [[Function]]s is that they can call themselves.
\
When a [[Function]] [[Call]]s itself it's called [[Recursion]], because when done like this by default it will recurse forever creating an infinite loop.
\
That happens because when you call a [[Function]] the [[Programming_Language]] will put it into memory on what's known as the [[Call_Stack]], which is a short-term chunk of memory for executing your code. When a [[Function]] keeps calling itself the language will keep pushing frames onto the call stack until you get a [[Stack_Overflow]] error.
\
To avoid this your [[Algorithm]] needs a [[Base_Condition]], so it knows when to terminate the loop.
\
Now when you write an [[Algorithm]], you'll need to determine if it's any good, and the system for doing that is called [[Big-O]] notation. It's a standard format for approximating the performance of an [[Algorithm]] at scale. It may reference [[Time_Complexity]], which is how fast your [[Algorithm]] will run and [[Space_Complexity]], which deals with how much memory is required to run it.
\
Developers have many different [[Algorithms]] types at their disposal. The most crude option is [[Brute_Force]], where you might loop over every possible combination to hack somebody's credit card pin.
\
A more sophisticated approach might be [[Divide_and_Conquer]], like [[Binary]] search, where you cut the problem in half multiple times until you find what you're looking for. 
\
Another option is [[Dynamic_Programming]] [[Algorithms]], where a problem is broken down into multiple smaller sub-problems and the result of each computation is stored for later use using a technique called [[Memoization]].
\
That means if a [[Function]] has already been called, it will use the existing value instead of recomputing it again from scratch.
\
Then we have [[Greedy_Algorithms]] that will make the choice that is most beneficial in the short term without considering the problem as a whole. One example of this is [[Dijkstra's_Shortest_Path]] [[Algorithms]]. 
\
On the flip side we have [[Backtracking]] [[Algorithms]], which take a more incremental approach, by looking at all the possible options like a rat in a maze exploring all the different potential paths.
\
Now when it comes to implementing your code there are always multiple ways to get the job done:
\
One programming paradigm is [[Declarative]], where your code describes what the program does, and the outcome, but doesn't care about things like control flow. 
\
This style of programming is often associated with [[Functional_Languages]] like "haskell".
\
The other paradigm is [[Imperative]] programming, where your code uses [[Statement]]s like "if", and "while".
\
Providing explicit instructions about how to produce an outcome is associated with procedural languages like, "c". Today most general purpose languages like [[Python]], [[JavaScript]], [[Kotlin]], [[Swift]] and so on, are [[Multi-Paradigm]], which means they support all these options at the same time, in addition to object-oriented programming.
\
The idea behind [[OOP]], is that you use [[Class]]es to write a blueprint for the data or [[Object]]s in your code.
\
A [[Class]] can encapsulate [[Variable]]s (_which are commonly called properties_), as well as [[Function]]s, which are usually called [[Methods]].
\
In this context it's a common way to organize and reuse code, because [[Class]]es can share behaviors between each other through [[Inheritance]] where a [[Subclass]] can extend and override the behaviors of the parent [[Class]] and it opens the door to all kinds of other ideas called [[Design_Patterns_Index]].
\
Now a [[Class]] by itself doesn't actually do anything, instead it's used to [[Instantiate]] [[Object]]s which are actual chunks of data that live in your computer's memory.
\
Often you'll want to reference the same [[Object]] over and over again in your code. When data is long-lived it can't go in the call stack, instead most languages have a separate area of memory called the "heap" which unlike the [[Call_Stack]] can grow and shrink based on how your application is used. [[Heap_Memory]] also allows you to pass [[Object]]s by reference. Which means you can use the same [[Object]] in multiple [[Variable]]s without increasing the memory footprint, because it always points to the same chunk of memory in the [[Heap_Memory]].
\
Now what's interesting is that if we go back to the [[CPU]] that we talked about in the beginning, you'll notice that it contains multiple [[Threads]]. [[Thread]]s take the physical [[CPU]] core and breaks it into virtual cores, that allow it to run code simultaneously.
\
There are some [[Programming_Language]]s that support [[Parallelism]], where you can write code that literally executes on two different [[Threads]] at the same time. However many languages out there are only single threaded, but that doesn't mean they can't do two things at the same time.
\
Instead they implement [[Concurrency]] models, like an [[Event_Loop]] or [[Co-Routines]] that can pause or delay the normal execution of code to handle multiple jobs on a single thread at the same time. Now in modern computing we're rarely working with the [[Bare_Metal]] [[CPU]] and [[RAM]], instead we work in the [[Cloud]] with a [[Virtual_Machine]], which is just a piece of software that simulates hardware.
\
That allows us to take really big computers and split them up into a bunch of smaller virtual computers. These machines are the backbone of the internet, and are connected via the internet protocol ([[IP]]) each machine has a unique [[IP_Address]].
\
To identify it on the network that [[IP_Address]] is usually alias to a [[URL]] that is registered in a global database called the "domain name service" ([[DNS]]).
\
Now to establish a connection, the two computers will perform a [[Career/Oops_Dups_Archive/2U_OSU_Bootcamp/Cysec_Notes/TCP]] handshake, which will allow them to exchange messages, called [[Packets]].
\
On top of that there's usually a security layer like [[SSL]], to [[Encrypt]] and [[Decrypt]] the messages over the network.
\
Now the two computers can securely share data with the "hypertext transfer protocol" ([[HTTP]]). The client may request a web page then the server will respond with some [[HTML]].
\
Modern servers provide a standardized way for a client to request data which is called an "application programming interface" or [[API]].
\
The most common architecture is [[REST]] where urls are mapped to different [[Data_Entities]] available on the server.
\
That brings us to our final topic: mother effin printers. You're gonna need to learn how these things work, inside and out, because every time you go to grandma's house she's going to ask you to fix it, which shouldn't be a problem for a computer scientist like you. Cheers!