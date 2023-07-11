# node-codeFlow
Node Js interview questions regarding code flow and the output of code snippets.

#### Write a program that reads a text file and returns the number of words in it using Node.js.
---
```
const fs = require('fs')
fs.readFile((err, data) => {
  const parsedData = data.toString();
  const numberOfWords = parsedData.split(" ").length;
  return numberOfWords
},
"..fileaddress")
```

#### Write a program that calculates the sum of two numbers passed as command line arguments.
---
```
const args = process.argv.slice(2);
const num1 = parseFloat(args[0]);
const num2 = parseFloat(args[1]);
```

#### Write the output for this code snippet.
---
```
function func1() {  
  let a = 1;  
  var b = 1;  
  for(let i = 0; i < 10; i++) {  
    setTimeout(()=>{  
      a = 1 + i;  
      b = 1 + i;  
      console.log(a, b);  
    },1000);  
  }  
}  
func1();
```
---
```
function test() {  
  let a = b = 0;  
  a++;  
  return a;  
}  
test();

// typeof a; // => ???  
// typeof b; // => ???
```
---
