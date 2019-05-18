# impatient-js

Notes on reading [impatient-js](http://exploringjs.com/impatient-js/index.html)

## Chapter 6 - Syntax

### Basics

- comments

```javascript
// single-line comment

/*
Comment with
multiple lines
*/
```

- bools

```javascript
true
false
```

- numbers
```javascript
1
1.3
-23
```

- strings - js has no char type!
```javascript
'bob'
"jim"
```

- assertions

```javascript
assert.equal(7+1,8)
```

`assert` is an object with an `equal` method - this is part of a Node.js assertion API.

- logging to console - both `log` and `error` seem to do same thing in node repl...

```javascript
console.log("hello")
console.error("this is an error")
```

- operators


```javascript
// logical 
true && false // AND
true || false // OR

// mathematical
3+4
5-1
2*3
assert.equal(9/2,4.5) // division is true division 
3 < 4
3 >= 3
assert.equal("abc" === "abc",true) // comparison without conversion
assert.equal(3 === "3",false) // comparison without conversion
assert.equal(3 == "3",true) // comparison with conversion
"def" !== "abc"

// strings
assert.equal("bob" + " jim", "bob jim")
assert.equal(3 + " bobs","3 bobs") // crazy JS type conversion!
```

- variable declaration

```javascript
let x // mutable declaration
x = 23 // assignment

let y = 54 // mutable declaration and assignment

const z = 23 // declaring z (immutable) - const must be declared
const z // SyntaxError: Missing initializer in const declaration
```

- `let` vs `var`

```javascript
for(var i=0; i<10; i++){
    console.log(i)
}
console.log(i) // this will log 10 `i` is still in scope
```

```javascript
for(let i=0; i<10; i++){
    console.log(i)
}
console.log(i) // ReferenceError: i is not defined
```

- control flow

```javascript
if (x < 0) {
    x = -x;
} // condition must be in parenthesis
```

- function def

```javascript
function foo(a,b) {
    return a+b
}
```

- arrow functions

```javascript
foo1 = (a,b) => a+b
foo2 = (a,b) => {return a+b}
```

- objects - mix of attributes and methods (like a class?)
```javascript
obj = {
    first: "bob",
    last: "bobson",
    getfull() {
        return this.first + " " + this.last
    }
}
```



