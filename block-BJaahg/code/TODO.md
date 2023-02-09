## Understanding Scope and the difference between var, let and const

Watch this video before doing the exercise: https://www.youtube.com/watch?v=XgSjoHgy3Rk

1. Guess the output:

```js
let firstName = 'Arya';
const lastName = 'Stark';
var knownAs = 'no one';

console.log(
  window.firstName,
  window.lastName,
  window.knownAs
);//  undefined undefined 'no one'
```

2. Guess the output:

```js
let firstName = 'Arya';
const lastName = 'Stark';
var knownAs = 'no one';

function fullName(a, b) {
  return a + b;
}

console.log(window.fullName(firstName, lastName));//AryaStark
```

3. Make a Execution Context Diagram for the following JS and write the output.

```js
function addOne(num){
  return num + 1;
}
var one = addOne(0);
var two = addOne(1);
console.log(one, two);//1 2
```

4. Make a Execution Context Diagram for the following JS and write the output.

```js
var one = addOne(0);
fucntion addOne(num){
  return num + 1;
}
var two = addOne(1);
console.log(one, two);// 1 2
```

5. Make a Execution Context Diagram for the following JS and write the output.

```js
console.log(addOne(0));//1
fucntion addOne(num){
  return num + 1;
}
var two = addOne(1);
console.log(two);//2
```

6. Make a Execution Context Diagram for the following JS and write the output.

```js
var one = addOne(0);
const addOne = (num) => {
  return num + 1;
};
var two = addOne(1);
console.log(two);
```

7. Make a Execution Context Diagram for the following JS and write the output.

```js
console.log(addOne(0));
const addOne = (num) => {
  return num + 1;
};
var two = addOne(1);
console.log(two);
```

8. What will be the output of the following

```js
function isAwesome() {
  var awesome;
  if (false) {
    awesome = true;
  }
  console.log(awesome);
}
isAwesome();//Undefined
```

9. What will be the output of the following

```js
function isAwesome() {
  let awesome;
  if (true) {
    awesome = true;
  }
  console.log(awesome);
}
isAwesome();//True
```

10. What will be the output of the following

```js
function isAwesome() {
  let awesome;
  if (false) {
    awesome = true;
  }
  console.log(awesome);
}
isAwesome();// Undefined
```

11. What will be the output of the following

```js
let firstName = 'Arya';
const lastName = 'Stark';
var knownAs = 'no one';

function fullName(a, b) {
  return a + b;
}
const name = fullName(firstName, lastName);
console.log(name);// AryaStark
```

12. Guess the output of the code below with a reason.

```js
function sayHello() {
  let name = 'Arya Stark';
}
sayHello();

console.log(name);//  ReferenceError: name is not defined, its becuase variable defined with keyword 'let' is function scoped and cannot be accessed outside of the function. 
```

13. Guess the output of the code below with a reason.

```js
if (true) {
  var name = 'Arya Stark';
}
console.log(name);// Arya Stark // variable defined with keyword var only creates function scope, it does not create block scope.
```

14. Guess the output of the code below with a reason.

```js
if (true) {
  let name = 'Arya Stark';
}
console.log(name);//  ReferenceError: name is not defined, unlike keyword var , let creates block scope , hence cannot be accessed from outside of block scope.
```

15. Guess the output of the code below with a reason.

```js
for (var i = 0; i < 20; i++) {
  //
}
console.log(i);// 20, variable defined with keyword 'var' is not block scoped and can be accessed from outside.
```

16. Guess the output of the code below with a reason.

```js
for (let i = 0; i < 20; i++) {
  //
}
console.log(i);// ReferenceError: i is not defined, unlike var, variables defined with the keyword let are block scoped and cannot be accessed from outside.
```

17. Guess the output and the reason behind that.

```js
function sample() {
  if (true) {
    var username = 'John Snow';
  }
  console.log(username);
}
sample();//John Snow, its because variable defined with keyword var is not block scope , making it posssible to acess value from outside.
```

18. Guess the output and the reason behind that.

```js
function sample() {
  if (true) {
    let username = 'John Snow';
  }
  console.log(username);
}
sample();//ReferenceError: userNme is not defined, unlike var, variables defined with the keyword let are block scoped and cannot be accessed from outside.
```

19. Guess the output and the reason behind that.

```js
function sample() {
  var username = 'Arya Stark';
  if (true) {
    var username = 'John Snow';
    console.log(username);
  }
  console.log(username, 'second');
}
sample();//John Snow , John Snow second // variable userName defined  with keyword 'var' and valiue 'Arya Stark' inside the function is overwritten by value 'john snow'.
```

20. Guess the output and the reason behind that.

```js
function sample() {
  let username = 'Arya Stark';
  if (true) {
    let username = 'John Snow';
    console.log(username, 'first');
  }
  console.log(username, 'second');
}
sample();// John Snow first  Arya Stark second // userName with the value 'arya stark' is global inside that vey function , whereas username with the value 'john snow' is limited to the block and cannot be accessed from outside.
```

21. Guess the output and the reason behind that.

```js
function sample(...args) {
  for (let i = 0; i < args.length; i++) {
    let message = `Hello I am ${args[i]}`;
    console.log(message);
  }
}

 //Hello I am First
 //Hello I am Second
 //Hello I am Third  
// rest operator (...) create an array and put all the arguments as an element inside that array, 

```

22. Guess the output and the reason behind that.

```js
function sample(...args) {
  for (let i = 0; i < args.length; i++) {
    const message = `Hello I am ${args[i]}`;
    console.log(message);
  }
}

sample('First', 'Second', 'Third');
//Hello I am First
 //Hello I am Second
 //Hello I am Third  
 // const keyword prevent re-assignment and not re-declaration, it is being declared and assigned a new value in each iteration of the loop.

```

23. Guess the output and the reason behind that.

```js
if (true) {
  const myFunc = function () {
    console.log(username, 'Second');
  };
  console.log(username, 'First');//  ReferenceError: Cannot access 'username' before initialization
  let username = 'Hello World!';
  myFunc();// 
}
```
The code console.log(username) will indeed throw an error "Uncaught ReferenceError: Cannot access 'username' before initialization" because the variable username is declared with the let keyword, which means it is subject to temporal dead zone (TDZ) rules.

TDZ rules state that a variable declared with let or const cannot be accessed before it has been declared in the same block of code. So in the code above, when console.log(username, 'First') is executed, username is in the TDZ and cannot be accessed, hence the error.

Once the declaration of username has been executed, the variable is no longer in the TDZ and can be accessed, as seen in myFunc().


 If there is an error in the code, subsequent code will not be executed, and the local execution context will not complete its entire execution.

In this case, since the error is thrown at console.log(username, 'First'), the code that declares the username variable and calls myFunc() will not be executed. The local execution context will stop executing at that point and the error will be propagated to the global execution context, which may handle the error in a way specified by the developer, such as by logging it to the console or displaying an error message to the user.
24. Guess the output and the reason behind that.

```js
function outer() {
  let movie = 'Mad Max: Fury Road';
  function inner() {
    console.log(
      `I love this movie called ${movie.toUpperCase()}`
    );
  }
  inner();
}

outer();
```

25. Guess the output and the reason behind that.

```js
function outer() {
  let movie = 'Mad Max: Fury Road';
  function inner() {
    let movie = 'Before Sunrise';
    console.log(
      `I love this movie called ${movie.toUpperCase()}`
    );
  }
  inner();
}

outer();
```

26. Guess the output and the reason behind that.

```js
function outer() {
  let movie = 'Mad Max: Fury Road';
  function inner() {
    let movie = 'Before Sunrise';
    function extraInner() {
      let movie = 'Gone Girl';
      console.log(
        `I love this movie called ${movie.toUpperCase()}`
      );
    }
    extraInner();
  }
  inner();
}
outer();
```

30. Using reduce find the final value when the initial value passed is `100`. You have to pass the output of one function into the input of next function in the array `allFunctions` starts with `addOne` ends with `half`.

```js
const addOne = (num) => {
  return num + 1;
};
const subTwo = (num) => {
  return num - 2;
};
const multiplyThree = (num) => {
  return num * 3;
};
const half = (num) => {
  return num / 2;
};

let allFunctions = [
  addOne,
  subTwo,
  multiplyThree,
  addOne,
  multiplyThree,
  half,
];

// Answer is: 447
```
