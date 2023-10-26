Source: https://www.youtube.com/watch?v=C2w45qRc3aU&t=80s


Monads are an extremely powerful design pattern that can be used without nearly any maths knowledge.
\
**All monads have 3 components:**

1. **Wrapper Type** - They should have a wrapper of some sorts, that marks the type of the monad. _(In the following example, its 'NumberWithLogs'.)_
2. **Wrap Function** - They should have some function that takes normal values, and wraps it up in the monad, effectively allowing entry to the monad ecosystem (Similar to a constructor). In broader parlance it's also known as either `return`, `pure`, or `unit`. _(In the following example, 'wrapWithLogs' played the role of the wrapping function.)_
3. **Run Function** - A function that takes the wrapper type and the transform function that accepts the unwrapped type and returns the wrapper type. In Broader parlance this is called `bind`, `flatMap`, or `>>=`. Its a bit easier to think of it as 'running', because it runs the transformation function on the argument passed in, doing 'monad work' behind the scenes, like for example, concatenation logs. _(In the following example that was 'runWithLogs'.)_
\
**What Are They?:**
	ex: (a couple of simple methods in TypeScript, one that squares a number and one that adds by one)

	// Starting Code:
	
	function square(x: number): number {
		return x * x
	}

	function addOne(x: number): number {
		return x + 1
	}

	// Starting Call:

	addOne(square(2)) => 5

Now lets say we wanted to add some historical logging to these functions, to show the process of how we got from 2 to 5 in this case.
\
The result would look something like this:

	// Call With Logging

	addOne(square(2)) => {
		result: 5,
		logs: [
			"Squared 2 to get 4.",
			"Added 1 to 4 to get 5."
		]
	}

You can see here that along side the result there is a 'logs' array, and each operation along the array has an element to show how the item got there. In real life this might be useful for an audit trail to show the operations that were carried out in code. But for this toy example were just manipulating numbers.
\
How should something like this be coded?:

	// First you should define a struct to capture the return type, which Here we'll call 'NumberWithLogs'. It will contain both the 'result' and the 'logs' array.

	// Code With Logging:
	
	interface NumberWithLogs {
		result: number
		logs: string[]
	}

	// Second we'll make the square function return a 'NumberWithLogs' and return the expected shape

	function square(x: number): NumberWithLogs {
		return {
			result: x * x,
			logs: [ `Squared ${x} to get ${x * x}.` ]
		}
	}

	// Third we'll change 'addOne' to take a 'NumberWithLogs' and perform an expected operation.

	function addOne(x: NumberWithLogs): NumberWithLogs {
		return {
			result: x.result + 1,
			logs: x.logs.concat([
				`Added 1 to ${x.result} to get ${x.result + 1}.`
			])
		}
	}

	// Since it's taking a 'NumberWithLogs' as the argument, we need to combine whatever logs came in with the new logs, by appending the new entry at the end. 

Although this works, there's still some issues with how this is written, first what if I want to do:
```
square(square(2))
```
it would return an error such as: 

```
Argument of type 'NumberWithLogs' is not assignable to parameter of type 'number'.
```
So it doesnt work because the first square returns a number with logs, but the second square expects just a number. Also What if I wanted to do something like:
```
addOne(5)
```
Then it would throw an error of:
```
Argument of type 'number' is not assignable to parameter of type 'NumberWithLogs'.
```
This wont work either because 'addOne()' expects a number with logs, not a normal number. However we can fix with with a new function called, 'wrapWithLogs()':

	// New Function:

	function wrapWithLogs(x: number): NumberWithLogs {
		return {
			result: x,
			logs: []
		}
	}

This new function takes a number and returns a number with logs, like a constructor of sorts. It helps 'numbers' enter the 'numberWithLogs' ecosystem, so to speak. So that one can call functions that expect 'numbersWithLogs'. This function sets the 'logs' to an empty array because nothing has been done yet. Now we can solve both problems that were talked about.
\
First we can change the function: 'squared take a number with logs' 

	// Tweaked Square Function:

	function square(x: NumberWithLogs): NumberWithLogs {
		return {
			result: x.result * x.result,
			logs: x.logs.concat([
				`Squared ${x.result to get ` +
					`${x.result * x.result).`
			])
		}
	}

This way we can execute 'square(square(2))', by doing 'square(square(wrapWithLogs(2)))'.
\
And to do 'addOne(5)' we just need to do, 'addOne(wrapWithLogs(5))'.
\
Onto the next issue, there seems to be some duplicated logic between 'square' and 'addOne'. Specifically, both of them are doing "log concatenation" (`x.logs.concat([])`).  
Is there a way to factor this out?
\
Of course, with a bit of ingenuity. First were going to move some stuff around to make square easier to read, its the same logic, just separated a little better:

	// Reorganized Square (same logic):

	function square(x: NumberWithLogs): NumberWithLogs {
		const newNumberWithLogs = {
			resultL x.result * x.result,
			logs: [
				`Squared ${x.result} to get ` +
					`${x.result * x.result}.`
			]
		}
		return {
			result: newNumberWithLogs.result,
			logs: x.logs.concat(newNumberWithLogs.logs)
		}
	}

This will help us see how our new function called 'runWithLogs' will help by handling the log concatenation for us.
So instead of the old call style which looks like this:

	// Old Call Style:
	addOne(wrapWithLogs(5))

We'll be using the new function like this:

	// New Call Style
	runWithLogs(wrapWithLogs(5), addOne)

While this seems like more code than just 'addOne(wrapWithLogs(5))', in a second you'll see how it takes a load off of 'addOne' and 'Square'.
\
From the use case and signature, you can see that 'runWithLogs' takes two arguments. The first is a 'number with logs', the second is a function to apply to a number, that returns a new number with logs. 

	// New runWithLogs Function:
	function runWithLogs(
	1. input: NumberWithLogs,
	2. transform: (_: number) => NumberWithLogs
	): NumberWithLogs {

Then the overall function returns a number with logs:

	// New runWithLogs Function:
	function runWithLogs(
		input: NumberWithLogs,
		transform: (_: number) => NumberWithLogs
	): NumberWithLogs {
	// Body:
		const newNumberWithLogs = transform(input.result)
		return {
			result: newNumberWithLogs.result,
			logs: input.logs.concat(newNumberWithLogs.logs)
		}
	}

Now lets walk through the body carefully.
First we run the transformation function, like 'addOne', on the number passed in, to get a new number with logs:

	const newNumberWithLogs = transform(input.result)

Then we take the number from it and use that as the result:

	result: newNumberWithLogs.result,

Then take the logs from the input we passed in and append any logs generated:

	logs: input.logs.concat(newNumberWithLogs.logs)

If you squint you can see how the latter part of the function:

	return {
		result: newNumberWithLogs.result,
		logs: x.logsconcat(newNumberWithLogs.logs)
	}

Is identical to the rewritten block in the 'New runWithLogs Function'.
All that's different is that we've taken the `Square`-esk part and moved it to the transform argument so it becomes more flexible. The net result of this is the 'addOne' & 'Square' do not need to do log concatenation anymore and become simpler. They also don't need to take a number with logs as an argument anymore and can just take a simple number.

	// Simpler Square Function:
	function square(x: number): NumberWithLogs {
		return {
			result: x * x,
			logs: [ `Squared ${x} to get ${x * x}.` ]
		}
	}

## Final Code Example:

	interface NumberWithLogs {
		result: number
		logs: string[]
	}

	function square(x: number): NumberWithLogs {
		return {
			result: x * x,
			logs: [ `Squared ${x} to get ${x * x}.` ]
		}
	}

	function addOne(x: number): NumberWithLogs {
		return {
			result: x + 1,
			logs: [ 'Added 1 to ${x} to get ${x + 1}.' ]
		}
	}

	function wrapWithLogs(x: number): NumberWithLogs {
		return {
			result: x,
			logs: []
		}
	}

	function runWithLogs(
		input: NumberWithLogs,
		transform: (_: number) => NumberWithLogs
	): NumberWithLogs {
		const newNumberWithLogs = transform(input.result)
		return {
			result: newNumberWithLogs.result,
			logs: input.logs.concat(newNumberWithLogs.logs)
		}
	}

With this setup we can combine arbitrary transformation in any order you like, which we couldnt do earlier, and we can add new transformation functions, like 'addTwo', or 'multiplyByThree' by just writing another function.
	ex:

	const a = wrapInLogs(5)
	const b = runWithLogs(a, addOne)
	const c = runWithLogs(b, square)
	const d = runWithLogs(c, multiplyByThree)

And these will work with our 'runWithLogs' without any additional effort.
Also on top of that with their handy 'runWithLogs' function, log concatenation is completely hidden away.
\
The tranformation functions like 'addOne' and 'Square', don't have to worry about log concatenation, because it all happens in one place; 'runWithLogs'.
\
You might be asking, "okay, this seems useful, but where are the monads?". You see, what was just written, IS a Monad. Monads at their core, are a helpful design pattern, and in this case this one is built from scratch.

**How Can They be Useful:**

They allow you to chain operations, like 'addOne', and 'Square', while secretly managing busy work, and other complex things, like in this case combining log entries. 

**Very Commonly Used Monad Examples:

To help and concrete the topic we can look at another very useful monad called 'Option' also known as 'Maybe'. (See. [[Rust-Monads_and_Option]])
\
It represents the possible non-existence of a value.
	ex:
	
	// A number has to be a number:
	number = a number

	// But an option of a number is a thing that might have a number in it or nothing at all.
	Option<number> = a number OR nothing

	// Similarly, an option of the user has either a user in it, OR nothing.
	Option<User> = a User OR nothing

It's like the fact that things can be null or undefined, but using an explicit type, which makes it safer and easier to check at compile time.
\
Going over the 3 monadic components that make up 'Option':

1. **Wrapper Type** - `Option<T>` It's going to be generic, which means that it can wrap any type. For example, it can wrap a number and get an option of a number (`Option<number>`), a string and get an option of a string (`Option<string>`), etc. You use the `<T>` to indicate that it's generic. In fact, most monads are generic in this sense. In the NumberWithLogs example could be improved to become generic as well (`NumberWithLogs` -> `ThingWithLogs<T>`). Since you can add logs to anything, not just numbers. 
2. **Wrap Function** -  This takes a 'thing' of type `<T>` and wraps it in an option, giving an option of the `<T>` (Turns `T`'s into `Option<T>`'s). In Option's case it's called sum, because it marks the thing as being something rather than nothing (Which is the value none).
3. **Run Function** - This accepts an option and a transformation function to run (just like what monads have). The only difference here is that the function is generic, which means it can work on options of numbers, options of strings, etc. (Runs transformations on `Option<T>`'s'). You can read `T` as the raw type, and `Option<T>` as the wrapped type. Just like the transform functions before, like 'Square', took a number (which is the raw type), and returned a number of logs (which is the wrapped type). The transform function here takes a `T` (The raw type) and returns an `Option<T>` (The wrapped type). 

Here's what the body looks like: If you pass an empty option (meaning it's none), it returns none. If you pass in something with a value in it, it runs transform on that value. This lets you chain operations without worrying about 'none' or 'null' values. 
\
To see how this may be useful, lets take an example where we may want to fetch the current user, get the user's pet, and then the user's pet's nickname, where all of those things could be missing.
\
Here's what it might look like without the Monadic Option:
	ex:

	function getPetNickname(): string | undefined {
		const user: User | undefined = getCurrentUser()
		if (user === undefined) {
			return undefined
		}

		const userPet: Pet | undefined = getPet(user)
		if (userPet === undefined) {
			return undefined
		}

		const userPetNickname: string | undefined = getNickname(userPet)

		return userPetNickname
	}

Here every time you run an operation, we need to check to see if the result is undefined, and short circuit to avoid continuing. 
The syntax: `User | undefined` means that the user variable is either a user or is undefined (which is often how missing values are represented in javascript), without using option. This code might ring a bell, given how often engineers need to handle 'missingness' in real code.
\
But it looks so much nicer when you use Monads:
	ex:

	function getPetNickname(): Option<string> {
		const user: Option<User> = getCurrentUser()
		const userPet: Option<Pet> = run(user,getPet)
		const userPetNickname: Option<string> = run(userPet, getNickname)
		return userPetNickname
	}

Assuming those get functions now return options. In this cose the true value of option becomes clear. No once in this code is undefined or things being checked manually. It all happens in run.
\
If user is nothing for example, 'userPet' and 'userPetNickname' will also be nothing, and 'getPet', and 'getNickname' will not be run. It's so convenient to be able to manage the lack of a value without constantly having to perform checks all over the place.
\
In some languages you can call run as a method on the option directly so the code becomes even cleaner, and more chainable.

![[Pasted image 20230605183249.png]]

So just try not to forget that:
Monads are a design pattern that allows `a user to chain operations` while `the monad manages secret work` behind the scenes.

![[Pasted image 20230605183417.png]]

Another example of how this code that accepts missing values Via Option:
```
	function getPetNickname(): Option<string> {
		const user: Option<User> = getCurrentUser()
		const userPet: Option<User> = run(userm getPet)
		const userPetNickname: Option<string> = run(userPet, getNickname)
		return userPetNickname
	}
```
Isn't even THAT much more code than a function that doesnt allow you to accept a missing value:

```
	function getPetNickname(): string{
		const user: User = getCurrentUser()
		const user: Pet = getPet(user)
		const userPetNickname: string = getNickname(pet)
		return userPetNickname
	}
```

**Common Monads Cont.:**

| Monad                   | Abstracts Away                                        |
| ----------------------- | ----------------------------------------------------- |
| NumberWithLogs / Writer | accumulation of log data                              |
| Option                  | Possibility of Missing Values                         |
| Future / Promise        | Possibility for values to only become available later |
| List                    | Abstract away branching computation                   |

Yes lists would be considered a monad in the way that in this example it helps you abstract away the wide variety of different outcomes from a combination of values. Like shown here:
	ex:

	const doors = [ 'red', 'green', 'blue' ];
	const doorAndCoinPossibilities = run(
		doors,
		door => {
			return [
				door + ' heads',
				door + ' tails'
			]
		}
	)

After running the code the door and coins possibility becomes this:

	[
	'red heads',
	'red tails',
	'green heads',
	'green tails',
	'blue heads',
	'blue tails'
	]

Even though some may say that lists are not a monad, that's okay its only a perspective to look at it, however despite that you can still happily use the 'run' function with your lists with flatMap:
\
**Example with `flatMap` (List's run function):**

	const doors = [ 'red', 'green', 'blue' ];
	const doorAndCoinPossibiities = doors.flatMap(
		door => [
			door + ' heads',
			door + 'tails'
		]
	)

**Explicit map, then flatten:**

	const doors = [ 'red', 'green', 'blue' ];
	const unflattenedDoorAndCoinPossibilities = doors.map(door =>
		[
			door + ' heads',
			door + ' tails'
		]
	)
	const doorAndCoinPossibilties =
		unflattenedDoorAndCoinPossibilites.flat()

So this is what `unflattenedDoorAndCoinPossibilites` would look like:
	![[Pasted image 20230605190909.png]]

