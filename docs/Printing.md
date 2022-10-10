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