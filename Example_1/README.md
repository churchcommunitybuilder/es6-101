# let & const
In ES6 we get two new types of variables; `const` and `let`. These two new types
have their own place but basically make `var` obsolete. One of the biggest
changes with `let` and `const` are they are both **block scoped**, this makes it
so if you declare either one inside of a block like an `if` or a blocked `case`
it wont be available out side of it.

```javascript
if (true) {
    let myValue = 5;
}

console.log(myValue); // undefined
```

Also there's a big difference between `let` and `const`. `const` will throw an
error if you try to reassign it to another value while `let` will let you change
the value as much as you want.

```javascript
// this works great
let a = 5;
a = 6;
console.log(a); // 6

// this doesnt work
const b = 5;
b = 6; // throws js error
```

But `const` only cares about its shallow reference to its value so you can still
change, for example, the properties of an object assigned to `const`.

```javascript
// this works great
const c = { x: 5 };
c.x = 6;
console.log(c.x); // 6

// this works too
const c = [3];
c.push(4);
console.log(c); // [ 3, 4 ]
```

## Assignment
- Create variables with `let` and `const`
- try them inside and outside of an if statement
- change the `let` variable value
- create an object with `const` and change or add a property on the object
- console.log at various points to show the values of the variables
