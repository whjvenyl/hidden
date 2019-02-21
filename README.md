# Hidden.js

With the aim to sensitise people to improve the accessibility of their websites, this script will make non-accessible elements invisible to everyone, until their accessiblity issues are fixed.

**If they can't read it, you can't see it.**

## How does it work

It uses the [axe-core](https://github.com/dequelabs/axe-core) accessibility engine to scan through the code and find accessibility issues.

Then, depending on the mode selected (`full` or `partial`), it either decreases the level of opacity of the entire page based on the number of errors found, or makes only the unaccessible elements totally invisible.

## How to use

To add the script to your project, add the following line in your main `js` file:

```javascript
import hidden from 'https://raw.githubusercontent.com/charliegerard/hidden/master/hidden.js';
```

Then, to start the script, write:

```javascript
hidden() // in which you can pass a mode option and a threshold of errors
```

```javascript
hidden('full', 2); // the full mode take a parameter for the max number of errors accepted;
```

```javascript
hidden('partial'); // partial does not need a max number of errors;
```

## Options

The script takes 2 arguments:

* A mode: `full` or `partial`
* A maximum number of errors tolerated.

If you don't specify these parameters when calling `hidden`, the default values will be used ('full' and 10).


