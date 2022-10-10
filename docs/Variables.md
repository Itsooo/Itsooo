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