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