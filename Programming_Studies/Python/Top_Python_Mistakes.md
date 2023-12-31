When coding in python make sure to be vigilant and not fall for these.

---
number 1: Manual string formatting
	Manual string formatting, aka putting things together with the plus sign. instead, use f strings. they're more readable, easier to write, and less prone to errors.

---
number 2: Manually closing a file
	Manually closing a file. i can't tell you tutorials recommend doing something like this. open the file, write to it, and then call close. if this write call throws an exception, the file will never be closed. instead use a with statement, which will ensure the file is closed even if an exception is thrown. on a similar note.

---
number 3: Using "try:" and "finally:" instead of a context manager
	Using try-finally instead of a context manager. i usually see this one from more experienced developers but coming from a different language. in python, most resources that need to be closed have their own context manager, use it. 

---
number 4: Using a bare "except:" clause
	Using a bare except clause. in python, keyboard interrupts and system exits are propagated using exceptions. that means, for  example, a bare accept is going to catch something like the user hitting ctrl-c. that's almost never what you actually want to do. if you still want to be lazy but you don't want to trap your user in a  box, then use an exit Exception, or if you want to do the right thing then catch the actual exception  that's going to be thrown. 

---
number 5: Thinking that "^" in python means exponentiation (it's a bitwise [[xor]], exponentiation is "a ** b")
	Thinking the carrot means exponentiation. nope, it's bitwise xor. okay, that one's a really newbie one, but I gotta pad the list somehow, right?

---
number 6: Use of default mutable arguments
	Any use of default mutable arguments. argument defaults are defined when the function is defined, not when it's run. in this case that means every call to the function is sharing the same list, meaning the second time we call it, it's not starting out as the empty list, it's starting out as the list containing zero from the previous call. probably not what you  wanted. if you want a mutable default, first set it to None and then check if it's None inside the function, setting the default there. 

---
number 7: Never using comprehensions, or only using list comprehensions
	Never using comprehensions, or if they do use comprehensions, only list comprehensions. a lot of code can be made both shorter and clearer by using comprehensions. you can have dictionary, list, set, and even generator comprehensions. learn how to use them when they're appropriate. 

---
number 8: ALWAYS using comprehensions
	_always_ using comprehensions. I get it, you just learned about comprehensions and now it's time to flex. but stop for a moment, you don't need to turn every single loop into a comprehension. sometimes this actually makes things less readable. i guess readability is really in the eye of the beholder, so you may not agree with this particular example, but i hope you can agree that not every loop should be turned into a comprehension. 

---
number 9: Checking for a type using " == "
	Checking for a type with = =. there  are some rare cases where you do want to do this, but most of the time this is not what you want. the reason is inheritance. a named tuple is a tuple, so this Point class is a tuple. but it's not literally the built-in tuple, it's a subclass. in most cases you should program in a way where  you should be able to substitute a subclass for its parent. this is called the Liskov substitution principle, and checking a type for equality is a violation of it. in most cases, what you  probably wanted instead was an is instance check. 

---
number 10: Using " == " to check for None, True, or False
	Using == to check for None, True, and False. instead of equality, you should check for identity using the is comparison. this is what == was going to do anyway, so just cut out the middleman and use is directly. 

---
number 11: Using an "if bool(x):" or "if len(x)" check
	Using an "if bool" or "if len" check. there's nothing particularly wrong about these. it's just that  they're usually equivalent to just a plain "if x" so using an "if bool" or "if length" check kind of just shows that you don't know the language that well. 

---
number 12: Using the "range(len(a))" idiom
	Using the "range length" idiom. a lot of beginners, especially those coming from other languages, think about loops in terms of indices. so they loop over the indices, but only ever use them to grab out the elements.  instead, just loop over the underlying container and get the elements directly. it's much easier to read and less error prone. if you did actually want to use the index though, you still shouldn't use range length. use enumerate to get the index and the element at the same time. another reason i see people use this is to use "i" as kind of a synchronizing variable to get corresponding elements from two different objects. of course, the better way to do that is using zip, and if  you still need the index use "enumerate zip". 

---
number 13: Looping over the keys of a dictionary
	Looping over the ".keys()" of a dictionary. don't you know, that's the default. if you're modifying the dictionary as you're looping over it, then it would be okay to make a copy of the keys. depending on the situation  this might add a little bit of clarity, but even in this case the ".keys()" is unnecessary. 

---
number 14: Not knowing about the dictionary items methods
	Not knowing about the dictionary items method. if you're looping over the keys of a dictionary and the first thing you do is grab the value out or each key, then what you really want is to loop  over the items of the dictionary, which are key value pairs. 

---
number 15: Not using tuple unpacking
	Not using tuple unpacking. do you have a tuple and want to get all of its elements out as separate variables? well you're  in luck. that's exactly what tuple unpacking does. 

---
number 16: Creating your own index counter variable
	Creating your own index counter variable. if you're starting at zero and adding one to something at the end of every loop, then once again what you really want is enumerate. 

---
number 17: Using "time.time()"" to time things
	Using time.time to time. I think we gotta give the noobs a break on this one. how are they supposed to know that time.time is not for timing your code? time.time is for telling you what time it currently is and it's not as accurate  as using perf_counter. subtracting two subsequent calls to perf_counter gives you the most accurate way of measuring how much time it took your code to run. 

---
number 18: Littering your code with print statements instead of using the logging module
	Littering your code with print statements instead of using the logging module. you can set up logging easily in your main function with your own custom format. you can also set the logging level or take it as a parameter so you can filter out messages that you're not interested in. there, doesn't that look a lot better? 

---
number 19: Using "shell = True" on any function in the subprocess library
	Using "shell=True" on any function in the subprocess library. "shell=True"  is the source of a lot of security problems, and let's be honest, the reason you probably did this in the first place is to avoid putting your arguments into a list. 

---
number 20: Doing maths or any kind of data analysis in Python
	Doing math, or pretty much any kind of data analysis, in python. learn to use [[Numpy]] for array operations and learn to use [[PANDAS]] for more general data analysis.

---
number 21: Using "import *" outside of an interactive session
	Using import * outside of an interactive session. import * usually litters your namespace with variables. instead, just import the things you actually need. 

---
number 22: Depending on a specific directory structure for your project
	Depending on a specific directory structure for your project. a lot of beginner code assumes that all of your source files are going to be in one flat source directory. they, probably unknowingly, are depending on the fact that when you import something python checks for it in your system path. python also adds the directory of the file being run to the path, so this usually works. however, this can really get you into trouble if you have multiple scripts that aren't in the same directory. take the time to learn how to package your code and install it into your current environment. 

---
number 23: The common misconception that Python is not compiled
	The common misconception that python is not compiled. have you ever seen those ".pyc" files next to your ".py" files? or maybe they were in a "__pychache__" directory. those files are compiled python code. but of course python is also an interpreted language, so what's going on? well python is compiled, but it's not compiled all the way down to machine code. instead, it's compiled to bytecode. that bytecode is then run by the interpreter. 

---
number 24: Not following PEP 8
	Not following [[pep8]]. pep8 is nothing more than a style guide, it doesn't actually affect your code at runtime. nevertheless, your co-workers, contributors, and friends will nag at you incessantly until you conform. at this point, whether it actually looks better or makes any difference at all is kind of irrelevant. experts do it this way to avoid the nagging.

---
number 25: Doing anything to do with Python 2
	Pretty much anything to do with python 2. python 2 hit its end of life years ago, and the only reason you should still be using it is if you already have millions of lines of python 2 written and it would be too much work to migrate. all new projects moving forward should be using python 3, and with that comes dispelling some rumors leaking over from python 2. even though x is really big, this code will execute instantly. ranges are not created in memory. even checking if something is in a range will happen quickly. given the endpoints of the range, you don't need to construct all the numbers to tell whether something is in that range, you just check how it compares to the boundary elements, and that's exactly what this in does. there are also things like the changed behavior of keys. this no longer creates a copy of the keys of the dictionary. instead, it produces a "view". that means if you delete a key, it'll no longer be in the view either.