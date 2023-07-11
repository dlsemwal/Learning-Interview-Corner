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
"..fileaddress")```

#### Write a program that calculates the sum of two numbers passed as command line arguments.
```
const args = process.argv.slice(2);
const num1 = parseFloat(args[0]);
const num2 = parseFloat(args[1]);
```
