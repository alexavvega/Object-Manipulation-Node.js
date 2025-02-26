# Object-Manipulation-Node.js


The sculptureListLengths object that I created - Wasn't really sure by what the instructions meant so I added it all here
--------------------------------------------------------------------------------------------------------------------------------
const sculptureList = require('./data.js'); // import data.js

// const element = sculptureList[1] <---- comment out this line in your solution!
/*this following snippet is just to show how to iterate an object's keys comment this out in your solution!
for (const key in element){
    console.log(`${key}: ${element[key].length}`)
} */

const sculptureListLengths = {};
const lengths = {};

sculptureList.forEach(sculpture => {
  for (const key in sculpture) {
    if (typeof sculpture[key] === 'string') {
      lengths[key] = sculpture[key].length;
    } else {
      lengths[key] = sculpture[key];
    }
  }
  Object.assign(sculptureListLengths, { [sculptureList.indexOf(sculpture)]: lengths });
});

console.log(sculptureListLengths);



{
  '0': { name: 26, artist: 20, description: 198, url: 31, alt: 90 },
  '1': { name: 17, artist: 16, description: 188, url: 32, alt: 91 },
  '2': { name: 16, artist: 19, description: 272, url: 31, alt: 98 },
  '3': { name: 4, artist: 14, description: 169, url: 32, alt: 96 },
  '4': { name: 9, artist: 20, description: 209, url: 32, alt: 98 },
  '5': { name: 13, artist: 16, description: 235, url: 32, alt: 90 },
  '6': { name: 9, artist: 21, description: 113, url: 32, alt: 94 },
  '7': { name: 11, artist: 18, description: 254, url: 32, alt: 95 },
  '8': { name: 15, artist: 14, description: 229, url: 31, alt: 92 },
  '9': { name: 15, artist: 15, description: 332, url: 32, alt: 86 },
  '10': { name: 7, artist: 15, description: 272, url: 32, alt: 98 },
  '11': { name: 6, artist: 10, description: 78, url: 31, alt: 92 }
}
