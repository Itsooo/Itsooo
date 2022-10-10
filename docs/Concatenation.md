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