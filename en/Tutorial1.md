# Learn to Program in Python

In this README file, there'll be many examples and fun tutorials for projects, these projects will help you learn & practice Python!

[Hint: Python comments start with `#` and end with a new line.]

Let's start with the most basic Python command, `print()`. 
`print()` is used to log & print text to the console. The syntax at it's most basic would be something like:

    print(string)

String is a placeholder for text, you can change it to anything.  Speaking of strings, let's check out our next Python tutorial.

[Hint: You can use variables in print statements!]

##
Strings are a collection of characters, they are enclosed like so:

    print("Hello World")
    # OR, like so:
    print('Hello World')

    OUTPUT:
    Hello World
    Hello World

Python supports both single and double quotes, the one you choose to use is up to you.

[Hint: Multiline comments start with `"""` and end with `"""`!]

##

So far, we've learnt about strings, and printing text. Next, the most important thing for most projects, `input()`.

`input()` is used to read the user's input. The way this command works is like this, picture it as a chart of events:

    get user input
                 > store it as a string
                                      > ready to use

For example, let's get a number from the user, try this code in your text editor/Repl:

    print('Give me a random number.')
    number = input("Your Number: ")

    print(number) #Prints user input

    OUTPUT:
    Give me a random number.
    Your Number: 4
    4

[Hint: The user must press enter to exit/submit input.]

`input()` can also be used as a "Press [ENTER] to continue" type of command. Here's an example!

    input("Press [ENTER] to proceed.")
    print("You proceeded!")

    OUTPUT:
    Press [ENTER] to proceed. #[ENTER PRESSED]
    You proceeded!

Now, we've learnt about `input()`, `print()`, and strings. Let's learn about functions!

##
Functions can be used to automate stuff. Let's create a function that will get the user's favorite colour.

    def askForColour():
      print("What is your favorite colour?")
      color = input("Colour: ")
      return color

Let's strip all of that for a better understanding.

`def` means 'definition', used to declare functions.

`askForColor()` is the function name, `()` is for parameters.

Everything behind `:` is what the function executes!

`return` is to give the value, so we can assign it to variables.

    userColour = askForColour() #Get colour
    print(userColour) #Print colour
    
    OUTPUT:
    What is your favorite colour?
    Colour: Red
    Red
    
More about functions later in the `Variables` section.
## 

In Python there is no specific command to generate variables, I will show you two methods to create variables.

- Dynamically (using functions)
- Manually

First, let's start with manually. To declare variables simply follow this syntax:

    variableName = value

`variableName` is what the variable will be refered to as, and `value` is what the variable stores.

Let's learn about `types`, there is 7 `types`.

- `str` - String
- `int` - Whole integer
- `float` - Decimal / Floating-point integer
- `bool` - Boolean (`True` or `False`)
- `list` - A list of values
- `tuple` - List of unorderable values
- `dict` - Dictionary (More info later on)

To convert one type to another, here is the basic syntax/most used conversion:

    #Convert int to str type:
    myInt = 5
    myString = str(myInt) #Returns as '5' instead of 5

    #Convert str to int type:
    myString = '5'
    myInt = int(myString) #Returns as 5 instead of '5'

Using the script above, you can convert type `int` to type `str` for printing purposes, or you can convert type `str` to type `int` for math operations.

Now let's take a look at function parameters and dynamic variables.

    def createVar(variableName, value):
      globals()[variableName] = value
      return globals()[variableName]

The `variableName` parameter is what the variable will be named. This parameter type is type `str`.

The `value` parameter is what the variable will be storing. This parameter type can be any type.

Let's test the script above:

    createVar('Username', 'ToasterCodes')
    print(Username)

    OUTPUT:
    ToasterCodes

Let's say our script is a module, it would be used like so:

    import myModule as module
    module.createVar('Variable', 'Hello world')

    print(module.Variable)

    OUTPUT:
    Hello world

[Hint: More about modules later on]

Why did we have to use the variable like `module.Variable`? Here's a simple explaination, the variable is stored on the module's memory instead of our program. So the variable is stored inside of the module. This is fixable like so:

    import myModule as module
    Variable = module.createVar('Variable', 'Hello world')
    
    print(Variable)

    OUTPUT:
    Hello world

Since our module's function uses the `return` keyword, we can store it as our own variable in our program's memory.

##

Test 1:

Create a program that gets two numbers from the user, and add them, and print them.

Grading:

- No Errors - 5 Stars
- 1 Error - 4 Stars
- 2 Errors - 3 Stars
- 3 Errors - 2 Stars
- 4 Errors - Failed

(These are just my grading rules, no need to use them!)
