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