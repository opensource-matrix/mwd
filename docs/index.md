MWD (Matrix Web Documentation) is a platform for documentating how code works, across programming languages and platforms.  Interested?  Feel free to check out any of the provided documentation!

## Syntax Highlighting
MWD uses syntax highlighting provided by [`MkDocs`](https://www.mkdocs.org).  Here's a few rich examples:
### NodeJs
```javascript
const fs = require("fs");
var textFile = fs.readFileSync("mytextfile.txt");
var textContent = toString(textFile);

/* Log to the console: */
console.log(textContent);
```

```python tab="PYTHON"
class MyClass:
    def __init__():
        print("Hello, world!")
    def goodbye():
        print("Goodbye, world!")


c = MyClass.new()
c.goodbye()
```
```php tab="PHP"
<?php
echo "Hello, world!";

class SayHello {
    public function __construct($name) {
        echo "Hello, " . $name;
    }
}

new SayHello("John Doe");
```

Thanks for reading the provided documentation! :)