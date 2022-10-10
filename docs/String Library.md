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