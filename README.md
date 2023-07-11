# node-codeFlow
Node Js interview questions regarding code flow and the output of code snippets.

###### Write a function to return number of words in a file
const fs = require('fs')
fs.readFile((err, data) => {
 const parsedData = data.toString()
const numberOfWords = parsedData.split(" ").length
}, "..fileaddress")
