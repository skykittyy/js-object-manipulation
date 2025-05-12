# Sculpture Script

This project processes a list of sculpture data and calculates the length of each property in every sculpture object. The result is a structured array (`sculptureListLengths`) that contains the length of each string property in the dataset.

---

##  File: `sculptureScript.js`

```js
const sculptureList = require('./data.js'); // import data.js

// const element = sculptureList[1] // <---- comment out this line in your solution!

const sculptureListLengths = [];

// this following snippet is just to show how to iterate an object's keys 
// comment this out in your solution! 
// for (const key in element){
//     console.log(`${key}: ${element[key].length}`)
// }

for (const sculpture of sculptureList) {
    let lengthObject = {};

    for (const key in sculpture) {
        lengthObject[key] = sculpture[key].length;
    }

    sculptureListLengths.push(lengthObject);
}

console.log(sculptureListLengths);

Output: sculptureListLengths
When the script is run with the data above, the following output is generated and printed to the console:

[
  { name: 13, artist: 12, description: 123 },
  { name: 9, artist: 14, description: 98 },
  { name: 10, artist: 11, description: 110 }
]
Each object in the array corresponds to a sculpture and shows the length of the string values in the name, artist, and description fields.
