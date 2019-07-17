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

