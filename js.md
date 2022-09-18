#### Variables

As far as JS is a dynamic weakly typed programming language we don't have to specify variable data type.

We have to just use keyword `var` | `let` | `const` to declare variable.

```js
var foo1;
let foo2 = 1;
const foo3 = 'foo3', foo4 = true;
```

#### Data types

There're 7 data types:

1. number
1. string
1. boolean
1. undefined
1. null
1. object
1. symbol

* How to check data type:

- `typeof`

```js
typeof 7 // "number"
typeof true // "boolean"
typeof ({}) // "object"
typeof null // "object" *well-know issue
```
___

* How to get the value of the last letter of the string:

```js 
const firstName = "Ada";
const lastLetter = firstName[firstName.length - 1];
```
___
##### String

- `split(str)`

```js
const str = "just some words";
const arrayOfWords = str.split(" ");
arrayOfWords // ['just', 'some', 'words']

const letters = str.split("");
letters // ['j', 'u', 's', 't', ' ', 's', 'o', 'm', 'e', ' ', 'w', 'o', 'r', 'd', 's']
```

##### Array

* How to create an array:

```js
const arr = [1, true, ['str']];
```
___

* How to get array element:

```js
const arr = [1, true, ['str', 2]];
arr[2] // ['str', 2]
arr[2][0] // 'str'
```
___
* How to update array element:

```js
const arr = [1, true, ['str', 2]];
arr[1] = false; 
arr // [1, false, ['str', 2]]
```
___

*  Access Multi-Dimensional Arrays With Indexes

```js
const arr = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
  [[10, 11, 12], 13, 14]
];

const subarray = arr[3];
const nestedSubarray = arr[3][0];
const element = arr[3][0][1];// element = 11
```
___

* To append element to the end of an array

- `push(element)`

```js
const arr = [1, 2, 3];
const res = arr.push(4);
arr // [1, 2, 3, 4]
res // 4 - length of updated array
```
___

* Remove the last element from an array and returns that element.

- `pop()`

```js
const arr = [1, 2, 3];
const res = arr.pop();
arr // [1, 2]
res // 3
```
___

* Remove the first element from an array and returns that element.

- `shift()`

```js
const arr = [1, 2, 3];
const res = arr.shift();
arr // [2, 3]
res // 1
```
___

* To append data to the beginning of an array

- `unshift(element)`

```js
const arr = [1, 2, 3];
const res = arr.unshift(0);
arr // [0, 1, 2, 3]
res // 4 - length of updated array
```
___
- `slice(startIndex, endIndex)`

Return copy of array part

```js
const arr = [1, 2, 3, 4];
const copy = arr.slice(0, 2);
copy // [1, 2]
```

Could be used for array cloning

```js
const arr = [1, 2, 3, 4];
const copy = arr.slice(); // [1, 2, 3, 4]
```
___
- `sort(function ownSort(a, b) {...})`


##### Object

* How to create an object:

```js
const obj = {
    someKey: "someValue",
    anotherKey: {
        anyKey: true
    }
};
```

* How to get object value by key:

```js
const obj = {
    someKey: "someValue",
    anotherKey: {
        anyKey: true
    }
};

const value = obj["someKey"]; // 1st way
const sameValue = obj.someKey; // 2nd way
```

* How to update object value by key:

```js
const obj = {
    someKey: "someValue",
    anotherKey: {
        anyKey: true
    }
};

obj["someKey"] = "someValue2"; // 1st way
obj.someKey = "someValue2"; // 2nd way
```

#### Conditions

Allow to change script flow by some "conditions".

```js
if (booleanExpression) {
    // code for true
} else {
    // code for false
}
```

Where `booleanExpression` - whatever could be converted into boolean.

For example:

```js
const logicalAndValue = true && false && true; // false
// true only when each item is true

const logicalToValue = true || false || true; // true
// false only when each item is false

const n1 = -4;
const n2 = -1;

if (n1 < 0 && n2 < 0) {
    // all numbers below zero
}
```

#### Loops

For repeating the code (any) multiple times

```js
for (let i = 0; i < 3; i++) {
    console.log(i);
}

// 0
// 1
// 2

for (let i = 3; i >= 0; i--) {
    console.log(i);
}

// 3
// 2
// 1
// 0

for (let i = 0; i < 5; i = i + 2) {
    console.log(i);
}

// 0
// 2
// 4

const arr = [1, true, "str"];
for (let i = 0; i < arr.length; i++) {
    const currEl = arr[i];
    console.log(i, currEl);
}

// 0, 1
// 1, true
// 2, "str"

```

#### Functions

A JavaScript function is a block of code designed to perform a particular task.

```js
function myFunction(p1, p2) {
  return p1 * p2; // The function returns the product of p1 and p2
}
```
Return Largest Numbers in Arrays
``` js 
function maxInArr(arr) {
  let max = -Infinity;
  for (let i = 0; i <arr.length; i++) {
    let current = arr[i];
    if (max < current){
      max = current;
    }
  }
  return max;
}

function largestOfFour(arrOfArrs) {
  let result = [];
  for (let i = 0; i <arrOfArrs.length; i++) {
    let currentArr = arrOfArrs[i];
    let currentMax = maxInArr(currentArr);
    result.push(currentMax); 
  }
  
  return result;
}

largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);
```

Repeat string N times

```js
function repeatStringNumTimes(str, num) {
  if (num === 0) {
    return "";
  }

  let res = "";
  for (let i = 0; i < num; i++) {
    res += str;
  }

  return res;
}

repeatStringNumTimes("abc", 3);
```

Truncate a string

```js
function truncateString(str, num) {
  if (str.length <= num)  {
    return str;
  }
  return str.slice(0, num) + "...";
}

truncateString("A-tisket a-tasket A green and yellow basket", 8);
```

Chunky Monkey, split array into sub-arrays by size N

```js
function chunkArrayInGroups(arr, size) {
  let result = [];
  let resultArrI = 0;
  for (let i = 0; i < arr.length; i++) {
    let curElem = arr[i];
    if (result[resultArrI] == undefined) {
      result[resultArrI] = [curElem];
    } else {
      result[resultArrI].push(curElem);
    }

    if (result[resultArrI].length === size) {
      resultArrI++;
    }
  }
  return result;
}

chunkArrayInGroups(["a", "b", "c", "d"], 2);
```

Find all array objects that has the same key(s)/value(s) as source.

```js
function whatIsInAName(collection, source) {
  const arr = [];
  // Only change code below this line
  const sourceKeys = Object.keys(source);

  const filtered = collection.filter((obj) =>
    sourceKeys.every((key) => obj[key] === source[key])
  );

  arr.push(...filtered);

  // Only change code above this line
  return arr;
}

whatIsInAName([{ first: "Romeo", last: "Montague" }, { first: "Mercutio", last: null }, { first: "Tybalt", last: "Capulet" }], { last: "Capulet" });
```

#### Prototype

```js
// The global variable
const s = [23, 65, 98, 5];

Array.prototype.myMap = function(callback) {
  const newArray = [];
  const targetArray = this.slice();
  // Only change code below this line

  for (let i = 0; i < targetArray.length; i++) {
    newArray.push(callback(targetArray[i]))
  }

  // Only change code above this line
  return newArray;
};

const new_s = s.myMap(function(item) {
  return item * 2;
});
```
