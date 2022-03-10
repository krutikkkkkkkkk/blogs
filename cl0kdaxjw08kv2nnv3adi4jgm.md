## Javascript Arrow Function

**JavaScript Arrow Function**
Arrow functions were introduced in ES6.

Arrow functions allow us to write shorter function syntax:

Before Arrow Function

```
function hello() {
  return "Hello World!";
}
```

After Arrow Function

```
let hello =()=> “Hello World”;
```

<hr>


***Arrow Function Syntax***

```
let myFunction = (arg1, arg2, ...argN) => {
    statement(s)
}
```


If the body has single statement or expression, 
you can write arrow function as:



```
let myFunction = (arg1, arg2, ...argN) => expression
```


It gets shorter! If the function has only one statement, 
and the statement returns a value, you can remove the brackets 
and the return keyword

<hr>


***Arrow Function with No Argument***

If a function doesn't take any argument, then you should use empty parentheses. for example,

```
let greet = () => console.log('Hello');
greet(); // Hello
```


***Arrow Function with One Argument***

If a function has only one argument, you can omit the parentheses. For example,

```
let greet = x => console.log(x);
greet('Hello'); // Hello 
```


***Arrow Function with more than one Argument***

```
let x = (x, y) => x * y;
```

<hr>

An arrow function expression is a compact alternative to a traditional function expression, but is limited and can't be used in all situations.

***Differences & Limitations:***

Does not have its own bindings to **this** or **super**, and should not be used as methods.

Does not have **new.target** keyword.

Not suitable for **call**, **apply** and **bind** methods, which generally rely on establishing a scope.

Can not be used as **constructors**.

Can not use **yield**, within its body.


<hr>

Thankyou



### Social  Links

Twitter: https://twitter.com/reboot13_dev

Instagram: https://instagram.com/reboot13_dev

Github: https://github.com/reboot13-git