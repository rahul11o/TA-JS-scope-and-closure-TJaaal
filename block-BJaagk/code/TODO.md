1. Convert the function below into different forms of function expression.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}

// Your code goes here
//First
// let percentage = function(marks, total){
//   return (marks * 100) / total;
// }

//Second
// let percentage = (marks, total) =>{
//   return  (marks * 100) / total;
// }

```

2. Write Function Declaration or Function Expression next to the function.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}
// Your answer
//Function Declaration
```

```js
let percentage = function percentage(marks, total) {
  return (marks * 100) / total;
};

// Function  Expression
```

```js
let percentage = function (marks, total) {
  return (marks * 100) / total;
};
//Function Expression
```

```js
let percentage = (marks, total) => {
  return (marks * 100) / total;
};
//Function Expression
```

```js
let percentage = (marks, total) => (marks * 100) / total;
//Function Expression
```

3. Why is a function definition an expression in JavaScript? Give one example of function expression.
// Because function defination is an object and since its an object, it can be stored in a variable and used as value.

eg.
let percentage = (marks, total) => {
  return (marks * 100) / total;
};
4. Why is a function call an expression in JavaScript?
In JavaScript, a function call is an expression because it returns a value. When a function is called, it is evaluated and the code within the function is executed. This can result in a value being returned from the function, which can then be used in the expression in which the function call appears. 

5. Write VALID and INVALID next to each example below with the reason.

```js
l

let five = add(2, 3); // Valid ,  end result of the function named add has been assigned to variable named five
five = add; // valid , variable five has been reassigned with a function reference named add;
five = five(10, 11); // valid , variable five has been reassigned once again.
five = function () {
  return 'Hello';
}; // Valid, the value of  variable five has been changed, which is ok to do.
```

6. What is the difference between function definition and function call? Explain with an example.
A function definition is a way to declare a function and giving it a name.
whereas function call actually execute the code which has been earlier defined in function defination.
eg..

```js
function percentage (marks, total) {
  return (marks * 100) / total;
};// it's a function definition

percentage(100, 500)// This is called execution.
```
7. What is the similarities between function definition and function call?
we use the same name  of the function when we are defining it and at the time of execution.
Both function definitions and function calls involve the use of the function keyword.
ction that has already been defined.

Both function definitions and function calls can take arguments

8. Is the code below valid or invalid. Explain with reason.

```js
function hello() {
  console.log('Hello World!');
}

hello.user = 'Sam'; // valid , its a valid function declaration in JavaScript.


```

9. What is higher order function explain with an example.
A higher-order function is a function in JavaScript that takes one or more functions as arguments, or returns a function as output.

10. Explain what is callback function. Why you can pass a function inside a function?
A callback function is a function that is passed as an argument to another function, and is executed after the outer function has completed.
You can pass a function inside a function because functions are first-class citizens in JavaScript, meaning they can be treated like any other data type (such as a string or number). This means that they can be assigned to variables, passed as arguments to functions, and returned as output from functions. 
