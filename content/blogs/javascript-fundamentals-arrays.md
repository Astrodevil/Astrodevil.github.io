---
title: "JavaScript Fundamentals: Arrays"
date: 2022-12-29T16:52:05+05:30
draft: false

series: ['JavaScript Fundamentals']
# weight: 2
# aliases: ["/first"]
tags: ["javascript", "tutorial", "webdevelopment", "100daysofcode", "programming", "coding"]
author: "Mr. Ånand"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: true
hidemeta: false
comments: true
description: "Day 10, 11 & 12 of #100DaysOfCode"

# canonicalURL: "https://blog.mranand.com/javascript-fundamentals-math-object"
disableHLJS: false # to enable highlightjs
disableShare: false
hideSummary: false
searchHidden: false
ShowWordCount: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowShareButtons: true
cover:
    image: "https://miro.medium.com/v2/resize:fit:1100/0*PT8ZWKHQgdccovV6" # image path/url
    alt: "Astrodevil" # alt text
    caption: "Photo By Mr. Ånand" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
editPost:
    URL: "https://github.com/Astrodevil/Astrodevil.github.io/tree/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

Today is the 12th day of my **#100DaysOfCode** journey with JavaScript.

I write about my learnings in an explained way through my blogs and socials. If you want to join me on the learning journey, make sure to follow my blogs and social and share yours too. **Let's learn together!🫱🏼‍🫲🏼**

This Article is a part of the [JavaScript Fundamentals](https://mranand.com/series/javascript-fundamentals/) series.

### Arrays

In JavaScript, we use arrays to store a list of elements. An array starts with an open square bracket `[` and ends with a closed square bracket `]`. The elements inside the array are separated by a comma `,`.

```javascript
const numbers = [1, 2, 3, 4];
const booleans = [true, false, true];
const strings = ["happy", "laugh"];
```

Arrays are mutable means they can be changed. In JavaScript, arrays are objects and can hold multiple values under a single name. Arrays can be stored under arrays, referred to as a nested array.

```javascript
const nested = [[2, 3, [2, 3]], 3];
```

While we are iterating over an array, we can keep a running value. We might do this for a variety of reasons. If we wanted to determine the average of several numbers.👇🏼

```javascript
const result = average([80,90,98,100]); 
console.log( result ); // 92
```

**Example:** Given an array, find the sum of all even values inside the array and return it.

```javascript
function sumEven(array) {
    let sum = 0;
    for(let i = 0; i < array.length; i++){
        if(array[i] % 2 === 0){
            sum = sum + array[i]

            }
    }
    return sum;
}
```

### Array Indexing

Arrays have zero-based indexes just like strings. This means that the first element in the array is at the index `0`, then 1:

```javascript
const element = array[0];
```

**Example:** Complete the function `hasOne` which takes in an array of numbers. Return `true` if any of the numbers in the `array` are `1`. Return `false` if not.

```javascript
function hasOne(array) {
    for(let i=0; i<array.length; i++){
        if(array[i] === 1){
            return true;
        }
    }
    return false;
}
```

### Return New Array

When formulating a function to filter an array, we can make a fresh array and insert the elements there whenever they meet our condition.

Let's imagine we wish to limit the numbers that an array returns to those that are bigger than 4:

```javascript
function greaterThanFour(array) {
    const newArray = [];
    for(let i = 0; i < array.length; i++) {
        const element = array[i];
        // is this element greater than 4?
        if(element > 4) {
            // yes, push this element on our array
            newArray.push(element);
        }
    }
    return newArray;
}
```

Here, we're making a new array and adding elements from the `array` to it only if they are greater than 4 to our `newArray`. The new array is then returned. `push` method adds new elements to the array.

**Example:** Write a function that will take an array of numbers and return a new array that only contains unique numbers.

```javascript
function unique(array) {
    let newArray = [];
    for(let i = 0; i < array.length; i++) {
        const element = array[i];
        if (newArray.indexOf(element) === -1) {
// indexOf method was learned in previous tutorial
            newArray.push(element);
        }
    }
    return newArray;
}
```

### Modify Array Values

Using square brackets like `array[0]`, we have learned how to read values from arrays. Similarly, we can use the assignment operator `=` to assign new values to those places.

```javascript
const array = [1,2,3];
array[0] = 6;
console.log(array); // [6,2,3]
```

**Example:** Complete the `addOne` function to add `1` to every element within the array. Since we are modifying the array directly do not return it.

```javascript
function addOne(array) {
    for(let i = 0; i < array.length; i++) {
        array[i]++;
    }
}
```

### Modify Array

Let's modify an array to filter it! `splice` method is used for removing elements from an array. Let's use `splice` to remove elements that are greater than `1`:

```javascript
const array = [1,2,3];
for(let i = 0; i < array.length; i++) {
    if(array[i] > 1) {
        array.splice(i, 1);
    }
}
console.log(array); // [1, 3]

// This is a Bug🐛
```

You must be wondering, why `console.log` showing `1` and `3` even after splicing elements greater than `1`. Let's see:

**Iteration 1:** The index points at the element `1`. We do not splice `1` because it is not greater than `1`. Works fine! `i=0`

**Iteration 2:** We find that `2` is greater than `1` so we splice at index `1`. Works fine! `i=1`

**Final Iteration:** Array length is `2` and `i=2`. Loop condition is that `i < array.length`, so there are no further iterations at this point. We never removed `3`!

* **Fix🔥**
    

By counting backwards.

```javascript
const array = [1,2,3];
for(let i = array.length - 1; i >= 0; i--) {
    if(array[i] > 1) {
        array.splice(i, 1);
    }
}
console.log(array); // [1]
```

**Iteration 1:** Starting from end, we remove `3` because it is greater than `1` . Works fine! `i=2`

**Iteration 2:** Let's move the index `i` to `1` . 2 will be removed by splicing at index `1` . Works fine! `i=1`

**Final Iteration:** `1` is not greater than `1`, so we do not splice it. We are left with `[1]` in our array, as expected!

### Conclusion

Ending with an extra bit of information about JavaScript functions...

JavaScript does not care if we modify a value inside the data structure when the word `const` is used with an object or an array. Arrays are objects, so you may also include arrays while discussing an object's characteristics.

**Today I learned about Arrays in JavaScript.**

#### If You ❤️ My Content! Connect Me on [Twitter](https://mobile.twitter.com/Astrodevil_) 
{{< bmc-button slug="Astrodevil">}}