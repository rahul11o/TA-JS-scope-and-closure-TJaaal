1. What does thread of execution means in JavaScript?
In javascript a thread of execution refers to the sequence of instructions that are executed in specific order one after other.


2. Where the JavaScript code gets executed?
Javascript code gets executed in  browser,s javascript engine.

3. What does context means in Global Execution Context?
'context', in global execution context refers to the environment in which javascript engine execute the code.

4. When do you create a global execution context.
whenever the javascript engine has to execute a code snippet or program, it creates a global execution context for once and all.

5. Execution context consists of what all things?
Execution context mainly consists of two things or in better way to say, it consists of two  sections, of which in first section, calculation,computation and execution happens and the other section is uesd as storage house for storing various kind of memory.

6. What are the different types of execution context?
There are two types of execution context - the global execution context and the function execution context.

7. When global and function execution context gets created?
Global execution context get created whenever theere is need to execute a code snippet or a program, it gets created just for one time whereas function execution context gets created multiple times depending upon the number of function to be executed in the given code snippet. whenever there is a need to execute a function, javascript engine creates a new function ecxecution context.
8. Function execution gets created during function execution or while declaring a function.
It gets created during the execution of function and not when it is defined


9. Create a execution context diagram of the following code on your notebook. Take a screenshot/photo and store it in the folder named `img`. Use `![](./img/image-name.png)` to display it here.



```js
var user = "Arya";

function sayHello(){
  return `Hello ${user}`;
}

var userMsg = sayHello(user);
```

<!-- Put your image here -->

![](./img/image-name.jpg)



```js
var marks = 400;
var total = 500;

function getPercentage(amount, totalAmount){
  return (amount * 100) / totalAmount;
}

var percentageMarks = getPercentage(marks, total);
var percentageProfit = getPercentage(400, 200);
```

<!-- Put your image here -->

![](./img/image-name.jpg)



```js
var age = 21;

function customeMessage(userAge){
  if(userAge > 18){
    return `You are an adult`;
  }else {
    return `You are a kid`;
  }
}

var whoAmI = customeMessage(age);
var whoAmIAgain = customeMessage(12);
```

<!-- Put your image here -->

![](./img/image-name.jpg)