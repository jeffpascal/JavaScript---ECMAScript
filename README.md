# JavaScript---ECMAScript

## var, let, const
- const is a replacement for var
- var gets moved up the lexical scope, they don't support blocked scope

- I have a loop, use a variable i after the loop.
- as if you delcared the i variable above the loop.
```js
function foo(){
  for(var i=0; i<10; i++){
  }
  console.log("i=" + i);
}
```

Hoisting example:
```js
    var customer = "Joe";
    (function (){
        console.log("1. The name of the customer inside the function is "  + customer);
         if (true) {
             var customer = "Mary";
         }
      
         console.log("2. The name of the customer inside the function is "  + customer);  
    })();

    console.log("3. The name of the customer outside the function is "  + customer); 
```
output:
```
"1. The name of the customer inside the function is undefined"
"2. The name of the customer inside the function is Mary"
"3. The name of the customer outside the function is Joe"
```


When you use **let** instead of **var** it introduces code block. (there is no hoisting)
- const is like let, but can be initialized only once

- const Example:
```js
const customer = "Joe";

  (function () {
      console.log("1. Inside the function " + customer);
      if (true) { 
        const customer = "Mary";
        console.log("2. Inside the block " + customer);
      }
 })();

console.log("3. In the global scope "  + customer);
```
output:
```
"1. Inside the function Joe"
"2. Inside the block Mary"
"3. In the global scope Joe"
```
- the const in the if statement is locked to that if statement.

- in this example

```js
function calcTaxES6(income, state = "Florida") {

  console.log("Calculating tax for the resident of " + state +
                                  " with the income " + income);
}

calcTaxES6(50000);
```
