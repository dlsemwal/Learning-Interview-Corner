# Important Interview topics in NodeJs
1. What is TypeScript, TS vs JS.
2. Webpack, tsconfig and usage.
3. Gulp / Grunt exposure and usage.
4. Closures and callbacks.
5. Promises and Async-Await
6. Single threaded behaviour of JavaScript / NodeJS
7. Event driven nature and event loop.
8. Blocking/ Non-blocking code and scaling.
9. Using EventEmitter for custom events.
10. AWS Keys, Roles, Policies.
11. AWS Lambda – Cold start, runtime, Layers
12. Lambda use cases.
13. DynamoDB – Database read/write and Index concepts.
14. SQS/SNS – Decoupling concepts
15. HTTPS – Encryption process between browser and server
16. Docker knowledge check
17. Third party integration – slow upstream scenario (High TPS to low TPS)

# Concepts
1. JavaScript Basics: Loops, Callbacks, iteration.
2. Closures – local variables
3. Scope using let / var / const
4. Usage of basic data structures – Array (Push/Pop) & Dict.
5. Recursion, Memoization
6. Space vs Time Complexity (Big O) – Stack / Hashmap
7. ES6/ES5 syntax
8. Candidates are expected to program using basic constructs of JavaScript instead of ES6 constructs. 

# node-codeFlow Questions
Node Js interview questions regarding code flow and the output of code snippets.

#### Write a program that reads a text file and returns the number of words in it using Node.js.
---
```JavaScript
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
```JavaScript
const args = process.argv.slice(2);
const num1 = parseFloat(args[0]);
const num2 = parseFloat(args[1]);
```

#### Write the output for this code snippet.
---
```JavaScript
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
```JavaScript
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
```JavaScript
var x = 10; 
var y = 20; 
function foo() { 
  var x = 30; 
  return function() { 
    console.log(x + y); 
  }; 
} 
  
var bar = foo(); 
bar();
```
---
```JavaScript
let item1 = {
 
  propertyA: { id: 13 },
 
  propertyB: "India",
 
};

let item2 = {
  property: "Singapore",
};

// join item1 and item2
```
---
```JavaScript
let result;
result = 1 == "1"
result = [1,2,3] == [1,2,3]
result = [9,4,8] == "9,4,8"
```
---
```JavaScript
const arr2D = [ [1,2][3,4][5,6]]
// flat the array
```
---
```JavaScript
 input: [3,5,1,4,2];
// return the max profit for different day stck price list
```
---
```JavaScript
function delay() {
 return new Promise((resolve) => setTimeout(resolve, 2000));
}
 
async function delayedLog(item) {
 await delay();
 console.log("Processing: ", item);
}
 
async function process(array) {
 array.forEach(async (item) => {
   console.log("Start process: " + item)
   await delayedLog(item);
   console.log("Processed: " + item)
 });
 console.log("Process completed");
}
process([1, 2, 3]);
```
---

