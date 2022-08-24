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

* How to get array element:

```js
const arr = [1, true, ['str', 2]];
arr[2] // ['str', 2]
arr[2][0] // 'str'
```

* How to update array element:

```js
const arr = [1, true, ['str', 2]];
arr[1] = false; 
arr // [1, false, ['str', 2]]
```

- `push(element)`

```js
const arr = [1, 2, 3];
const res = arr.push(4);
arr // [1, 2, 3, 4]
res // 4 - length of updated array
```

- `pop()`

```js
const arr = [1, 2, 3];
const res = arr.pop();
arr // [1, 2]
res // 3
```

- `unshift(element)`

```js
const arr = [1, 2, 3];
const res = arr.unshift(0);
arr // [0, 1, 2, 3]
res // 4 - length of updated array
```

- `shift()`

```js
const arr = [1, 2, 3];
const res = arr.shift();
arr // [2, 3]
res // 1
```

- `slice(startIndex, endIndex)`

Return copy of array part

```js
const arr = [1, 2, 3, 4];
const copy = arr.slice(0, 2);
copy // [1, 2]
```

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
