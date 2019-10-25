title: Error
description: Print to the console in Javascript.

!!! info
    This is also supported by Node.

!!! info
    This is a builtin class, you don't need to load any libraries to use it.

!!! danger
    This will break your code if you aren't using it correctly!

### `Error`
The `Error` class allows you to log an error and stop the rest of the code.

!!! Usage
    ```javascript
    new Error([string message [, string fileName [, number lineNumber]]])
    ```

## **Properties**
<code>Error.prototype.constructor</code><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The function that initializes the class.<br>
<code>Error.prototype.message</code><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The error message.<br>
<code>Error.prototype.name</code><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The name of the provided error.

## **Vendor-Specific**
### **Microsoft**
<code>Error.prototype.description</code><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Similar to the `message` property.<br>
<code>Error.prototype.number</code><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The error number.<br>
### **Mozilla**
<code>Error.prototype.fileName</code><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Path of the file that raised this error.<br>
<code>Error.prototype.lineNumber</code><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The line number of which this error occurred.<br>
<code>Error.prototype.columnNumber</code><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The line number of which this error started.<br>
<code>Error.prototype.stack</code><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Stack trace.<br>

## **Methods**
<code>Error.prototype.toSource()</code><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Returns the source of the specified Error object as a string.<br>
<code>Error.prototype.toString()</code><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Returns a string describing the object.  Overrides the builtin `toString()` method.<br>

Let's say you are making a library for something, you need to make sure that everything is accounted for, including the arguments of a function.  This example shows how you may go about handling that situation.  Remember, you need to `throw` the error for it to do anything.
```javascript
function myFunction(val) {
    if(typeof val == "undefined") {
        throw new Error("myFunction() requires exactly one argument.")
    }
    // ...
}

myFunction() // > [Error]
```

Or, maybe you want to catch an error.  Try this:
```javascript
try {
    throw new Error("Hello, world!")
} catch(e) {
    print(e.message) // e.prototype.message
    // > Hello, world!
}
```