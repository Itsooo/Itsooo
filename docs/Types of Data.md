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