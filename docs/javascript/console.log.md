title: console.log
description: Send an error to the console in Javascript.

!!! info
    This is also supported by Node.

!!! info
    This is a builtin method, you don't need to load any libraries to use it.

### `console.log`
`console.log` is a method that allows you to write to the console, whether it's in Node or in your web browser's developer console.

!!! Usage
    ```javascript
    console.log(tuple args)
    ```

It accepts any number of arguments and joins them together with a blank space (`" "`), then prints them to the console.  Let's check out some examples:
```javascript
/* Just one argument */
console.log("Hello, world!")
// > Hello, world!
```

```javascript
/* Multiple arguments */
console.log("Hello,", "world!")
// > Hello, world!
```

```javascript
/* With a variable */
var name = "John Doe"
console.log("Hello,", name)
// > Hello, John Doe
```

```javascript
/* With a function */
function hello(name) {
    console.log("Hello,", name)
}

hello("John Doe")
// > Hello, John Doe
```