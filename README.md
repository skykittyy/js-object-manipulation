# js-object-manipulation

const sculptureList = require('./data.js'); // import data.js

//const element = sculptureList[1] // <---- comment out this line in your solution!

const sculptureListLengths = []; 

// this following snippet is just to show how to iterate an object's keys
// comment this out in your solution!
//for (const key in element){
    //console.log(`${key}: ${element[key].length}`)
//}

for (const sculpture of sculptureList) {
    let lengthObject = {}; 

    for (const key in sculpture) {
        lengthObject[key] = sculpture[key].length; 
    }

    sculptureListLengths.push(lengthObject); 
}

console.log(sculptureListLengths); 

