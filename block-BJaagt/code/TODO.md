Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

Example:

```js
function hello() {
  var username = 'Arya';
}
console.log(useranme); // Reference Error username is not defined
```

In above code we are looking for the variable named `usename`. There is no variable named `username` in the global scope. The variable is inside the function named `hello` and we can't access the variable defined inside a function from outside.
The above code will throw an error sying `Reference Error username is not defined`.

2. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
{
  const username = 'Arya';
}
console.log(useranme); //Reference Error username is not defined
```
Variable created with the keyword const inside the block is scoped, hence its uses is limited  only inside the block scope and cannot be accesed from outside.

3. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
if (true) {
  let username = 'Arya';
}
console.log(useranme); // /Reference Error username is not defined.
```
If statement creates block-scope, hence any variable defined inside if statement with the keyword 'let' and 'const' cannot be accessed from outside, if tried, will thrown a referance error.
4. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
if (true) {
  var username = 'Arya';
}
console.log(useranme); //Arya
```
Keyword 'var' is not block-scoped as the keyword 'let' and 'const' , hence variable created inside using  'var'  inside block would not be scoped and can be used globally.

5. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
var username = 'Arya';
let username = 'John';
if (true) {
var username = 'Arya';
}
console.log(username); //  Identifier 'username' has already been declared
```
If a variable is already defined using keyword 'let' in a scope, you cannot define the same variable second time in the scame scope, if done it would throw an error saying "  Identifier 'username' has already been declared".
6. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = 'John';
if (true) {
  let username = 'Arya';
}
console.log(username); // "john"
```
If you are creating the same variable with same or different value in two different scope, that's allright to do.

7. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = 'John';
function sayHello() {
  let username = 'Arya';
}
sayHello();
console.log(username); // john
```
Variable created with the keyword 'let' inside the function is scoped and got nothing to do with stuff goung outside that function.

8. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
for (var i = 0; i < 10; i++) {
 console.log(i, 'First');
 // 0 'First'
//  1 'First'
//  2 'First'
//  3 'First'
//  4 'First'
//  5 'First'
//  6 'First'
//  7 'First'
//  8 'First'
//  9 'First'
}
console.log(i, 'Second'); // 10, second
```

9. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
for (let i = 0; i < 10; i++) {
  console.log(i, 'First'); 
//  0 'First'
//  1 'First'
//  2 'First'
//  3 'First'
//  4 'First'
//  5 'First'
//  6 'First'
//  7 'First'
//  8 'First'
//  9 'First'
}
console.log(i, 'Second'); // 'i' is not defined.
```
