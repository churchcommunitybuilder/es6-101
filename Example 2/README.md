# Arrow functions
In es6 we have a new shorter way to declare functions, its called the arrow
function. The arrow function is useful for more than just being shorter though.
Lets start by seeing what it looks like.

```javascript
const add = (x, y) => {
    return x + y;
};

console.log(add(2, 3)); // 5
```

But it can also be compressed down, if you only have one argument you can omit
the parens and if you only have one statement you can omit the curly brackets
and the return keyword. When you dont have curly brackets whatever your
statement evaluates to will be automatically returned.

```javascript
const addOne = x => x + 1;

console.log(addOne(2)); // 3
```

Also you can have arrow functions that return more arrow functions

```javascript
const add = x => y => x + y;

const add5 = add(5); // y => 5 + y;

console.log(add5(2)); // 7

console.log(add(3)(6)); // 9
```

But its even more than syntastic sugar. The arrow function will auto bind to the
`this` in the current context, no more guessing what `this` is.

```javascript
const myObject = {
    aFunc: function() {
        button.onclick = function() {
            console.log(this); // button
        };
    },
};

const myObject = {
    aFunc: function() {
        button.onclick = () => {
            console.log(this); // myObject
        };
    },
};
```

## Assignment
- create an arrow function with multiple arguments that does some simple math
  including all the arguments, use it and console.log the output
- create an arrow function with only one argument and divides it by 42, dont use
  parens or curly brackets, console.log the output
- create an arrow function that returns an arrow function that returns an arrow
  function (ception...), and does some simple math with the 3 arguments. Use it
  with a console.log, should look something like `console.log(myfunc(3)(4)(5))`
