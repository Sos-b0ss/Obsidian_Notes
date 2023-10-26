"Do **[[Drive-by_Attacks]]** actually **exist** within **modern** **browsers** and if yes how do they work?"
\
It is absolutely possible, and there is a big market for it. As NULL mentioned, no one is going to burn a 0day just to show you, but you can look at countless patched vulnerabilities. Google for any [[MFSA]] ([[Mozilla_Foundation_Security_Advisory]]) for anything that says "[[Arbitrary_Code_Execution]]" or "[[Potentially_Exploitable_Crash]]". These are all vulnerabilities (security bugs), not exploits (code to take advantage of said security bugs).
\
The way they work varies. It would be too difficult to explain even the basics of any number of classes of vulnerabilities. Look into [[Buffer_Overrun]]s/[[Buffer_Underrun]]s, [[UAF]]s, [[ROP]] (and similar techniques like [[JOP]] and [[LOP]]), [[Heap_Spraying]], [[JIT_Spraying]], [[Exploitable_Undefined_Behavior]], [[Integer_Overflow]]s, or any other common **attack** technique.
\
I found a lot of blog posts, forum discussions etc. but none of them actually give real examples. They simply talk about how JavaScript is a programming language so it isn’t predictable.
\
What they are likely talking about is things like [[Buffer_Overflow]]s and [[Use-After-Free_Vulnerabilities]]. They mean that JavaScript does not always do what you want it to **do**, not that the standard itself isn't entirely deterministic.
\
[[JavaScript]] isn’t unpredictable in a way that let’s it do things it’s not supposed to. Unless of course there is a vulnerability in the **[[Browser]]**.
\
That is correct. [[JavaScript]] is not designed to do anything outside of the context of a **[[Browser]]**, but what it _is_ designed to do is be parsed and compiled from [[Attacker-Controlled_Sources]]. A single bug in the [[Interpreter]] or [[JIT_Compiler]] (among many other things) can result in exploitation. This isn't just an issue with [[JavaScript]]. [[CSS]] and [[HTML]] can also be exploited, though that's less common as they're simpler. [[WebGL]] is a common target due to its complexity. [[Image_Decoding]] is also a target.
\
"Show me code that would for instant delete all the photographs on my machine without me having to explicitly download and run anything. Just visiting a malicious website is enough."
\
If you want an example of actual code, how about https://github.com/cryptostorm-dev/torsploit, which was used by the US government to **attack** outdated versions of Tor **Browser** (which is based on Firefox) a while back. In that specific example, it caused the **browser** to phone home, bypassing the proxy. The shellcode could be modified to do anything, such as delete pictures on your computer like you said. Honestly, I don't care enough to write shellcode to do something like delete pictures, but it would not be hard. The hard part is getting the code to execute. The easy part is making it do whatever you want.
\
In that specific example, the shellcode is in the `magneto` variable. You can change it to whatever you want and it will be executed without restrictions. All you have to do is learn a bit of assembly, enough to write the code without the help of the usual assembler. You can find a huge amount of pre-written shellcode for plugging into a working exploit, though usually it does more interesting things than delete pictures, like install malware.
\
The way that specific exploit worked was by using a type of heap spraying called JIT spraying (a technique to increase the predictability of the memory layout of the target program), and a simple buffer overflow into the now-predictable code.
\
See https://www.exploit-db.com/search/?action=search&description=Mozilla%20Firefox for countless other examples, complete with code. If you want **in**-depth explanations of how this kind of exploitation is done, I strongly recommend you read some **browser**-related Phrack articles.
\
And no, simply making my **browser** crash without any permanent damage on my computer doesn’t count.
\
Unfortunately, virtually all exploitable bugs will result in a harmless crash if they are not designed specially to exploit the application. Most PoCs will show nothing but a crash. You have to live with that. There are absolutely real, weaponized exploits that you can use, but there are not as many in public.
\
And to be clear: I only care about **browser** vulnerabilities, not plugins or other things. And also **modern** **browsers** not IE from 2004 (you know what, let’s just ignore IE).
\
Virtually every single update for a **modern** **browser** fixes one or several of these kinds of vulnerabilities. As of this post, Firefox 56 has just updated to fix 5 exploitable crashes with mfsa2017-21, as well as a collection of 12 other potentially exploitable memory-safety crashes. This isn't just an issue of one possibly bad bug every 10 years. This is multiple exploitable bugs every release. In general, _any_ large program which parses complex data can be exploited with malicious crafted input if someone tries to find a vulnerability badly enough. This applies to **browsers**, image decoders, video or audio decoders, and even your operating system kernel.