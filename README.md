# node-codeFlow
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
