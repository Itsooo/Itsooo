# Luau
Luau is a language that is made for Roblox in November 2021 that is derived from Lua 5.1 but has some cooler features, these features include: Ternary Operators (if a then b else c), Better compiler optimizations so code is runs a lot more efficiently even if you code doesn't include any sort of micro optimizations and lastly one of the big changes is that Luau is typed (not strict although you can set it optionally) unlike Lua which makes catching errors by the Linter a lot easer.

## Note
Some information to know before hand is that scripts run line by line ascending from 1 to infinity (or how many lines of code there are in your script)

# Printing
Printing is a **function** that does the task of putting what you input (**arguments**) in to the **output**.

## Use Cases
Printing is useful for troubleshooting/debugging as it can help us narrow down the problem area, for example if we've got an error in our code that's causing it to crash. By using a series of `print` statements we can see exactly where the script crashes and hopefully work out why. This process is known as **debugging**. Printing also doesn't just tells us where our code reaches but also tells us the information that we input like the value of the **data** or the type of **data** depending on what we choose to input, so if we ever want to know what sort of value something is we can use printing for that.

## Syntax
The syntax or structure of printing follows the same rule as calling a **function** in the future that being the name of the function in this case the name is `print` (YOU HAVE TO MAKE SURE ITS EXACT like cascing and all the LSP or auto fill will help you find the right wording) followed by parenthesis `()` the inside of the parenthesis is where you will be inserting your **arguments** an example of this would be 
```lua
print("Hello World!")
```
This would print "Hello World!" in the **output**. You might be confused as to why we need the double quotes `""` but just think of them as a way for us to represent characters to the program.

### Multiple Arguments
As said before functions aren't maxed out by 1 **argument** we can have multiple of them and we can separate them using commas (do not that the **convention**/norm is to add a space after the comma)
```lua
print("Foo, bar, baz", 42)
```
This would print out both `Foo, bar, baz` and `42` in a way like this in the output `Foo, bar, baz	42` do note that the comma only separates the **arguments** if its not included in the type of **data** your using, so in this case the commas in the words `Foo, bar, baz` is not separated by the print since it's on the inside of the double quotes it's only when its out when its recognized as a separator instead of being included in the phrase/**string**.

## Vocab
- **Function:** A function is something  that you call to do a certain task for you given the inputs (**arguments**) and returns a value/**data** in return if programmed to do so. -- More one functions later on.
- **Output:** A place where your scripts messages go *e.g. prints and errors*.
- **Argument:** An Argument is the input you put in a function which are separated by comma for different arguments.
- **Data:** Data is information that a computer can take in that is based of 4 **MAIN** types (string, number, bool, nil). -- More on types later on.
- **Syntax:** Syntax is the type of structure that is needed by the computer/program so it knows what you are trying to do.
- **String:** A string is a line (or **string**) of characters used represent a letters/numbers/symbols. -- More on strings later .

# Comments
Comments is a way to get characters you write to not be recognized b the program. I want to include this now rather than later because I will be using it code snippets to explain what something does.

## Use Cases
Comments are typically used for explanations or complex code so any readers reading the code can understand. You might think this is useless, but there are times where you don't look at your code for a long time and you get lost as to what does what, so comments are an easy way better understand code. Do note that too much comments can clutter your code especially if your explaining something super easy the only exception is if you are teaching the reader how to use their code and such for open source things.

## Syntax
The syntax for comments is two dashes `--` followed by the text you want to display `Lorem Ipsum Dolor Sit Amet`
```lua
-- This is a comment anything shown here is not run!
print("Hello") -- This can also go to the right of yoru code!
```
Comments are also typically one space apart from your code if you have it on the same line if not then no extra spacing is needed. It is also typical to have a space after the two dashes for better readability. Do note that just using dashes will be one line and will make anything to the right of the dashes be a comment even if its part of code like this.
```lua
print("Oh" -- "noooo!!", 42)
print("Doesn't work like this though -- since the dashes are part of the phrase/string")
```

### Multi-line comments
If you want a comment to have a definite end or multi-lined you can use multi-lined comments which follows similar syntax to single lined ones. The syntax would be the two dashes followed by two open bracket `--[[` the text is then followed `Foo` which is then closed by two closed brackets `]]` an  example of this would go as followed.
```lua
--[[
This
Is
Multi
Lined!
]] print("Has a definite end so you can place code after brackets (even though you shouldn't)")
```

# Types of Data
Types of Data are basically types of data some of the main ones that make up everything the ones that we will be going over are **strings, numbers, bools, nil.**

## Use Cases
Data is used in EVERYTHING and you won't be able to make anything without them. We will be going over the uses of the types in their own sections

## Strings
Strings are basically a line or **string** of characters. A quick way to remember them would be to relate them to quotes as quotes have everything like numbers, letters and symbols (or literally anything that you can type and is part of UTF8). We use strings as they give us ways to display text or prints even like displaying intermission or showing the name of a player etc.

### Syntax
The syntax  for **declaring** (making) a string is by getting a peace of text `42.._@da_` and enclosing them in quotes `"" or ''`  do note that if you start with a single quote or double quote you have to end with that exact quote it can't be changed.
```lua
"Bar"
'Foo'
"I LOV3 ROBLOX"
```

#### Escape Characters
You might notice that if you add the same quote symbol inside the string then the program will think you are ending the quote even though you don't. If you want to add something like a quote inside a string but don't want to obstruct it, you can use escape characters for that. An escape character will negate any sort of effect a character has with the syntax in this case the string. The escape character for Luau would be the backslash `\` behind the character you want to negate.
```lua
"no way a quote in a string?? --> \"real!!\" If you print this out would not include the backslashes but if you want to include them you just backslash them again"
"oh no!!I don't know what escape characters are !! " noooooo " erroooor"
```
There is an exception however and that is if your using a different quote than the one your using in string it will not error
```lua
"woah' 'n'o'w'a'y' 'n'o' 'e'r'r'o'r's'!'!'!"
```

#### Multi-line strings
Something that is not as known/used is multi lined strings which is used if you want some multi-line action you will have to incorporate some brackets. The syntax for this would be double brackets enclosing the piece of text yo want `[[text]]`
```lua
"
non 
multi
"
[[
YES
MULTI
With "quotes!"
]]
```
However if you for some reason have another set of double brackets inside your string you can use escape characters or make your string have a different start and end which you can do by having equal signs `=` in-between  like so
```lua
[=[
Its [[all]]
possible
]=]

[==[
You can also [[incorporate]]
[=[more]=] equal signs if needed!
]==]
```

### New Line
If you want to represent a new line in a string but don't want to use multi line strings? Well the character `\n` breaks the line making a new one!
```lua
"Up\nDown" --[[ How its represented if you print or use vv
Up
Down
]]
```

## Numbers
Numbers are quite self explanatory they are used for **arithmetic**/math especially since game development is centered heavily on it.

### Syntax
The syntax also in itself is quite self explanatory you put type in the number you want `n` and if you want to do something like addition or subtraction you can type out the operator `Add +, Sub -, Multiply *, Divide /, To the power ^`. It is also **convention**/norm to type out a space between operators since it makes it more readable the only exception being `^` Luau like any other programming language follows PEMDAS instead of just going left to right. **NOTE** do **NOT** use commas when using numbers as they will error

```lua
42 -- this is a number
15 + 10 -- 25
2^3 -- 8
10 / 2 -- 5
10 + 2^2 * 5 -- 30
```
Also something quick to note decimals used as well initiated with decimals with no limitations as well
```lua
10. -- viable
11.5 -- viable
11.0 -- viable
```

#### Special Notation
Numbers can also be displayed using scientific notation `1e5` if you don't want to type out all the extra zeros
```lua
1.5e8 -- 150,000,000
```
If you have trouble trying to type out precise but big numbers without  commas you can substitute it for underscores `_` to make it more readable
```lua
123_456_789 -- 123456789
```

## Bools
Bools are very simple as they are simply either true or false. They are usually used to check if something is on or off like if an ability is on cooldown or 

### Syntax
The syntax is also quite simple for a value to be true it has to have the keyword of `true` if its false then the keyword will be `false` you have to make sure however that it is the right casing or else it will think your calling something else
```lua
false -- this is false!
true -- this is true!!
```

## Nil
Nil simply means nothing this is something also used in other languages except its None instead of Nil. It is used to display well nothing like if you reference an object that is not there or get a value that doesn't exist. Nil also has a sort of relationship with false especially when it comes to conditionals which we will get to later.

### Syntax
The Syntax is quite simple if you want to have something displayed as nil or nothing you simply type out the keyword `nil` you also have to make sure the casing is the same in this case its all lowercase.
```lua
nil -- This is nothing or nil!
```

## Vocab
- **Convention:** The norm or the usual pattern which would be the one you should use.
- **Arithmetic:** A part of math that consist of operations such as addition, subtraction, division and multiplication.

# Concatenation
Concatenation is the act of joining two **operands** (values) together this is typically used for conjoining strings but can also be used for numbers.

## Use Cases
Concatenation is most definitely useful as it is used to alter a sort of prompt like 95% of the time. An example of this is if your doing something like an intermission and you have the prompt of 'Starting in: ' and you have the value that corresponds to it, you can concatenate it profit.

## Syntax
The syntax follows the same sort of syntax if you would add two values together but instead of using the operator of `+` you change it to `..` and like adding the **convention**/norm is to add spaces before and after
```lua
print("This is now " .. "with this!") -- This now with this!
print("The answer is: " .. 42) -- The answer is: 42
print(1 .. 1) -- 11
```
Something to note is that the only main types of data you can concatenate are numbers and strings the rest will result in an error. Although if you do want this sort of behavior for other types than you can use the `tostring` function to convert them in to strings which can be concatenated.
```lua
print("The answer is: " .. tostring(false)) -- The answer is: false
```

# Variables
Variables are a place in your computer (**memory**) that  holds a certain value (**data**) which can be called to at any point in time.

## Use Cases
Variables are probably gonna make up a huge portion of your code. The reason we need them is because we need them to save values to use them later like lets say I want to save the amount of times a player jumps we can use variables for that we can also use it to make code shorter and more readable by breaking things down in to smaller pieces. We can also use variables to save **constant** (things that don't change) like gravity we can use a variable rather than instead of just writing the number each time which would make it more confusing as well as less efficient.

## Syntax
- **Declaring:** When it comes to **declaring** (creating) a variable you have to start with the keyword `local` the reason we include this is for scope reasons but just think of it as a way to make your code more efficient. what follows is the name of the variable `myVariable` which we separate with a space (the **convention**/norm is just one space). There are some **rules** when naming variables those are:
	- No starting a variable with a number since it would thing you are trying to declare a number which we are not. You can however include numbers after the first character of your variable
	- No symbols in variables (only exceptions being underscores `_` )
```lua
-- Good!
local _myVariable2 -- this creates a spacec in memory for _myVariable2!
```
```lua
-- Bad!
local 2myVari@ble! -- this will error as it includes a number at the beginnign and symbols!
``` 
- **Assigning:** When it comes to **assigning** (setting) a value to a variable it is quite simple, you include an equal sign `=` after you refer to the variable (you can assign a value when you declare the variable or after depends largely on the situation, and spaces aren't necessary but its the **convention**/norm to include spaces before and after an equal sign) which is then followed by the value you want to set it to `"Value"`
- **Calling:**  Calling is simply when you retrieve the variable to do stuff with it in our case we call out variable to set a value to it to call a variable you simply mention it's name. Also one requirement to calling a variable is that it actually has to be declared before you call it else it will just return nil
```lua
-- Good!
local myVariable = 10 -- Creating myVariable and making it equal to 10

local myVariable2 -- Declaring myVariable2
myVariable2 = 42 -- Assigning myVariable to 42

print(myVariable, myVariable2) -- 10	42

myVariable = myVariable + 5 -- we assign/change myVariable to myVariable(10 at the time) + 5 which would = 15

print(myVariable) -- 15
```
```lua
-- Bad!
print(myVariable) -- nil
local myVariable = 10

newVariable = true -- although this won't error its not recommended and will result in a bunch of linter errors which makes up a good portion of what old code used to look like for roblox
```

### Compound Assignments
Compound assignments are shortcuts that are specific to Luau to make the process of using operators on variables. The syntax is a bit funky but easy if you break it down, so first we have to know what we are doing so lets say for example we have this 
```lua
local myVariable = 10
myVariable = myVariable + 90

print(myVariable) -- 100
```
to turn this in to a compound assignments we add the operator we want before the equal sign so in our case it would look like `+=` like if your shifting the `myVariable +` all the way to the left so only the `+` survives also do note you can only do this after you declare and assign your variable as they are only used when you want to alter your variable. It is also recommended to use this type of assignment is possible as it makes your code a lot shorter and readable
```lua
local myVariable = 10
myVariable += 90

print(myVariable) -- 100
```

### Multiple Assignments
This type of assignment is when you want to assign multiple things at once, this is usually used when you want to swap the values of something. The syntax might seem a bit confusing at first but just make sure to link the variables from order left to right, so the syntax goes at follows, first the variables you want to assign `var1, var2` followed by an equal sign of course `=` and then the values you want to set it to `10, 15` . As I said before this is usually done to swap two variables but you can also see it when someone wants to group similar variables together for compactness
```lua
-- Without multiple assigments
local var1 = 10
local var2 = 20

local oldVar1 = var1 -- we save the value for var1 because it gets overrited when we assign it to var2
var1 = var2
var2 = var1
-- this causes unecessary clutter in your script and doesn't work in some cases

print(vat1, var2)
```
```lua
-- With Multiple assigments
local var1 = 10
local var2 = 20

var1, var2 = var2, var1

print(vat1, var2) -- 20		10
```
```lua
local startNum, endNum = 0, 20 -- an example of using multiple assignments when declaring

print(sstartNum, endNum)
```

### Special Cases (tuples)
There are some cases in which a **function** (a refresher on functions is that a function is something that you call to do a certain task for you given the inputs (**arguments**) and returns a value/**data** in return if programmed to do so) In our special case the function we call doesn't return just one value but multiple! This means that we will need more variables to be declared in the same spot to fill up all the space that the other values. The syntax would be the variable name then a comma and then the variable name that will hold the next value in line going from left to right
```lua
local value1, value2 = returns2Things() -- pretend this functions returns  1	2

print(value1, value2) -- 1	2
```
```lua
-- if we just put one variable
local value1 = return2Things()

print(value1) -- 1
```
If for some reason you might want value2 but not value1 you can name the first variable an underscore `_` this is **convention**/norm for variables you don't need to use but need to place/name in order to get the value you want. The reason we use underscores is because it won't pop up in the autofill
```lua
-- just value2
local _, value2 = return2Things()

print(value2) -- 2
```
Also something not that important but also happens is that since it returns two values that are seperated by a comma and a comma also seperates arguements you can use them in other functions (excluding the ones you make for some reason) or ***tables*** like so
```lua
print(return2Things()) -- 1   2
-- same as
print((1, 2) -- 1   2
```

# String Library
The string **library** is basically a list of functions that are based of strings, like if you ever wondered how to manipulate or figure out if a string has something the string library is there for you! Although there are plenty and they all have their uses I'm just going to go over the main ones that you will use if you want to learn more go here -> [string (roblox.com)](https://developer.roblox.com/en-us/api-reference/lua-docs/string)

## Use Cases
The string library is used sometimes but when you do use it, its super helpful some cases in which you might you use a string library would be like admin commands where you want to autofill or something of that manner but there also others especially in GUI related things.

## Syntax
The syntax goes as followed. Firstly you type in the library you want to use in our case we want to use the string library so we type out `string` you have to make sure its typed exactly like that since its case sensitive and all. Right now we have called the `string` library with all the functions we want. What we want to do is access one of these functions and to do that we put a period `.` to show we want to access/**index**/retrieve something inside and then we type out the name of the function we want to use `funcName` and of course like all functions we have encountered before (print) we use parenthesis `()` to tell the program what we want to input to our function
```lua
string.example()
```

### String Structure
Something to know before moving on is that strings in Luau/Lua have numbers that are designated to each character, meaning the first character in our string would be identified as 1 the second would be 2 so on so forth.
```lua
-- 1 3 5
  "string"
--  2 4 6
```

### string.len()
string.len len would be short for length basically gets the length of a string, but since we use this function A LOT Lua decided to also make it a unary operator meaning that if you put the operator `#` behind the string it will give you the length. If you still don't know what unary operator means just think of the negative sign and how it just affects one operand (number in this case) which makes sense since unary is short for one and operator basically means the symbol that does the operation
```lua
print(string.len("123456")) -- 6
-- asame result
print(#"123456") -- 6
```

### string.sub()
string.sub is used to get a part of a string or section the two inputs (plus the string that your are also going to input) are where the slice begins and where it ends
```lua
--                        1 3 5
local slice = string.sub("SLICED", 2, 5) -- starts slice at the 2nd character and ends it at the 4th
--                         2 4 6
print(slice) -- LICE
```
There is also some other functionality to it but I would again forward you to look at the string documentation

### string.rep()
string.rep is used to repeat the string that you input and repeats it by the amount of the times you input
```lua
local repeated = string.rep("RE", 4) -- repeats "RE" 4 tiems

print(repeated) -- RERERERE
```

### string.find()
string.find tries and find if the string that you first put in matches with the string that you input second and if it does it will give you the indices of where it found it first going from left to right, however if it doesn't find it will return nil
```lua
--                                  1 3 5 7 9
local foundS, foundE = string.find("The quick brown fox", "quick")
--                                   2 4 6 8
print(foundS, foundE) -- 5	9
```
Also a thing to know if you don't want to be as strict and want to have some generality when it comes to the pattern string you can look in to string patterns which aims to solve that exact issue. I can't go in to it in depth here but if you want to know how to do that I would recommend going here -> [String Patterns (roblox.com)](https://developer.roblox.com/en-us/articles/string-patterns-reference)

### string.match()
string.match serves the same purpose for string.find the only difference is that instead of returning of returning the indices it gives you the string thing that matched with the pattern you fed it. This would be much better suited with string patterns
```lua
local match = string.match("The quick", "qui")

print(match) -- "qui"
```

### string.gsub()
string.gsub is used to replace any sort of pattern that you feed it. There is a lot more that goes in to the input but the basic thing is. This as well is also much better suited with string patterns. This would also replace endlessly unless told otherwise with the extra **argument**
```lua
local replaced = string.gsub("I hate roblox!", "hate", "love") -- replace hate with love

print(replaced) -- I love roblox!
```

### string.format()
string.format is very powerful and is a bit complicated due to its flexibility if you want to know more go here -> [Formatting and Converting Strings (roblox.com)](https://developer.roblox.com/en-us/articles/Format-String)

## Method Alternative
I hear you this is a lot of typing and Lua also thought about this and integrated the string functions in to the string itself and the way you call them is by typing out a colon after the string `:` then like before we call the name of the function `funcName` the only difference after that is that we don't have to include the first argument that being the string we want to utilize since when we call the function it already knows the string its on and will perform the action on it
```lua
local sub = ("SLICED"):sub(2, 5) -- cuts it to the second character to the 5th like last time

print(sub) -- LICE
```
Now you might be asking "Wait what's with the parenthesis covering the string is it really necessary?" Well lets check how we would normally do this and then work our way from their
```lua
local myString = "SLICED"
local sub = myString:sub(2, 5)

print(sub) -- LICE
```
As you can see from this example it doesn't need the parenthesis, why is that? Well when you call a variable the program automatically interprets it as if it were covered by parenthesis. The reason? The reason is that we want to compute whatever is inside our variable FIRST and then do whatever else is needed on to the variable so in the top example we need the parenthesis so the program knows that we want to do something with this string if that makes sense. If it still doesn't you can look at this example
```lua
local compute = 5 + 10 -- 15
-- It would just make sense that its 30 right?
print(compute * 2) -- 30

--this is because this is basically doing
print((5 + 10) * 2)
```

## Vocab
**Library:** A library is basically a **table** of functions that fit the libraries purpose (in our case we use the string library to better use strings).
**Table:** A table is basically a list that holds **elements**/**values**/**data** that can be **indexed**/retrieved at certain points by typing the corresponding value. -- More on how we produce tables later as they are a big topic

# Math Library
The math library  has the same concept as the string library but with math related things. There is a lot more than shown here so if you would like to look at more you can go here -> [math | Roblox Creator Documentation](https://create.roblox.com/docs/reference/engine/libraries/math)

## Use Cases
The Math library is pretty useful especially if you need to do some complicated equations or any sort of trigometric functions.

## Syntax
The syntax is basically the same as the string library but instead of putting `string` we put `math` you also have to make sure its all lowercase or it will not work.
```lua
math.something(42)
```

### math.huge
If your not really into math this one is probably the one you will use, math.huge is **NOT** a **function** but rather a **property** that is part of math. A property is a value that is stored in to a certain table or object in our case `huge` is a property of `math`. The main syntax that differs from a **function** and a **property** is that to call a property you don't need to include the parenthesis `()`. Aside from the syntax math.huge is a way of writing infinity
```lua
print(math.huge) -- inf
```

### math.pi
math.pi is self explanitory, it is a property like math.huge and it represents pi
```lua
print(math.pi) -- 3.14159265358979323...
```

### math.random()
math.random as the name implies it will get a random number, the first arguement is the minimum and the second is the maximum
```lua
print(math.random(1, 10)) -- returns a number between 1 and 10 NO DECIMALS
```
do note if you put not arguments in math.random it will return a number between 0 and 1. Also do note that there is another alternative to getting random numbers which is Random.new() but it is a bit more complicated but gives you more options, more on that here -> [Random | Roblox Creator Documentation](https://create.roblox.com/docs/reference/engine/datatypes/Random) There is also another type of random which is **noise** Roblox does have a function for this but its a bit complicated to explain so I would recommend looking it up, it is kind of like math.random but instead of it being all random its more smoothed out.

### math.min()
math.min returnjs the smallest number out of the numbers you input. man.min is not just limited to two **arguments** but multiple
```lua
-- selects the smallest
print(math.min(50, 5)) -- 5
print(math.min(10, 5, 2, 42)) -- 2
```

### math.max()
math.max has the same concept as math.min except it picks the biggest number instead of the smallest.
```lua
print(math.max(5, 50, 25, 100)) -- 100
```

### math.clamp()
math.clamp basically limits a number from going out of a certain range and basically clamping/holding it down it passes or goes below a certain point. It has three the first one is the number the second one is the minimum point it can reach and the third is the maximum point it can reach.
```lua
print(math.clamp(10, 0, 1)) -- 1
-- prints 10 because it goes over 1 meaning it will have to clamp down to 1
```
a thing to note is that the second **argument** must ALWAYS be less than the third or else it will error.