title: Functions
description: Learn how to use functions in Javascript!

!!! help
    This is a tutorial.  Feel free to follow along!

!!! info
    This is also supported by Node.

Functions in Javascript are used to help prevent repetetive code.  Let's pretend you have two Javascript files.  One loads the other when it's needed.  That's basically what a function is, but it's all in one file.

Let's get started by making a function called `HelloWorld`.  Remember, the code in the function should be inside of the function definition, like so:
```javascript
function [NAME]([ARGUMENTS]) { // <-- FUNCTION DEFINITION
    // CODE HERE!!!
} // <-- END OF FUNCTION DEFINITION
```

So, can you guess how we're going to make our `HelloWorld` function?  Before reading the code below, just guess.
Now let's see if you're right!  If you guessed something like this:
```javascript
function HelloWorld() {
    // ...
}
```
### **Congratulations!**
You did it!  Now, let's make it do something.  We're just going to print "Hello, world!" for now, using the [`console.log`](../console.log) inbuilt method.  It should look somewhat like this.  Feel free to print out anything you want!
```javascript
function HelloWorld() {
    console.log("Hello, world!")
}
```

!!! warning
    Don't forget to call your function!  Put this below your function definition.
    ```javascript
    HelloWorld()
    ```

## **Arguments**
Okay, you figured out how to make a function!  But what if you want to process something the user sent?  I'll show you how.  You know how I put the `[ARGUMENTS]` thing in the brackets (`()`<-- those things)?  Well that is where we are going to define our arguments.  Also, you can concatenate strings with the `+` operator.

```javascript
function HelloWorld(name) {
    // `name` is the name of someone you want to say hello to. ;)
    console.log("Hello, " + name)
}
```

Let's call the function!
```javascript
function HelloWorld(name) {
    // `name` is the name of someone you want to say hello to. ;)
    console.log("Hello, " + name)
}

HelloWorld("John Doe")
// > Hello, John Doe
```

## **Optional Arguments**
