---
title: "JavaScript Fundamentals: While Loop, Break and Questions for Practice"
date: 2022-12-22T16:52:05+05:30
draft: false

series: ['JavaScript Fundamentals']
# weight: 2
# aliases: ["/first"]
tags: ["javascript", "tutorial", "webdevelopment", "100daysofcode", "programming", "coding"]
author: "Mr. Ånand"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: true
draft: false
hidemeta: false
comments: true
description: "Day 7 of #100DaysOfCode"

# canonicalURL: "https://blog.mranand.com/javascript-fundamentals-math-object"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowBreadCrumbs: true
ShowWordCount: true
ShowPostNavLinks: true
ShowShareButtons: true
cover:
    image: "https://miro.medium.com/v2/resize:fit:1100/0*vSJC1LAMSN3VdyVr" # image path/url
    alt: "Astrodevil" # alt text
    caption: "Photo By Mr. Ånand" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
editPost:
    URL: "https://github.com/Astrodevil/Astrodevil.github.io/tree/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

Today is the 7th day of my **#100DaysOfCode** journey with JavaScript.

I write about my learnings in an explained way through my blogs and socials. If you want to join me on the learning journey, make sure to follow my blogs and social and share yours too. **Let's learn together!🫱🏼‍🫲🏼**

This Article is a part of the [JavaScript Fundamentals](https://mranand.com/series/javascript-fundamentals/) series.

### While Loop

As long as the test condition evaluates to `true`, the while statement generates a loop that performs the provided statement. Before the statement is carried out, the condition is assessed.

```javascript
while(b > 7) {
    // do something
}
```

We are just stating that if a condition is `true`, this statement shall be carried out till it is not.👇🏼

**Example:** Complete the `top` double function to find the largest double for the `value` that is below the `top`.

```javascript
function topDouble(value, top) {
   
    while (value < top) {
        value = value*2;
       
    }
    return value/2;
}
```

### Break Statement

We will exit the loop once `break` is hit. Even when the condition is `true`, there is still a possibility to exit the loop thanks to the `break` statement.

```javascript
while(true) {
    if(a > 5) {
        // exit the loop
        break;
    }
}
```

### Questions for Practise

* Given an integer value **num**, determine if it is even. If it is even, return `true`. Return `false` otherwise.
    
    ```javascript
    function isEven(num) {
        if (num % 2 === 0){
        return true;
        } 
    }
    
    // or
    
    function isEven(num) {
        return num % 2 === 0;      
    }
    ```
    
* The function `smallerNumber` will be given two unequal numbers: `num1` and `num2`. Your goal is to find the smaller number and return it!
    
    ```javascript
    function smallerNumber(num1, num2) {
    if (num1 < num2){
        return num1;
    }
    else {
        return num2;
    }
    }
    ```
    
* A string is stored in the variable `fakeName`. Take this fake name and use it to replace every occurrence of `"John"` in the `message`. Do not change the message in other way.
    
    `const fakeName = require('./fakeName');`
    
    ``const message = ` Hello, John! You left a package at the office today. You can pick up tomorrow at 10am, John. If not I will drop it off this weekend. Goodbye John! `;``
    
    ```javascript
    const fakeName = require('./fakeName');
    
    const message = `
        Hello, ${fakeName}! You left a package at the office today.
        You can pick up tomorrow at 10am, ${fakeName}. 
        If not I will drop it off this weekend.
        Goodbye ${fakeName}!
    `;
    ```
    
* The function `checkNumber` takes a single argument: a number `num`. The function should return the string `positive` if the number is positive, `negative` if the number is negative, and `zero` if the number is zero.
    
    ```javascript
    function checkNumber(num) {
        if (num > 0){
            return 'positive';
        }
        else if(num < 0){
            return 'negative';
        }
        else {
            return 'zero';
        }
    }
    ```
    
* The function `maxSum` takes a number argument `num`. Your goal is find the sum all of numbers, starting from 1, up to and including `num`.
    
    ```javascript
    function maxSum(num) {
        let sum = 0;
        for(let i=1; i<=num; i++){
            sum = sum + i;
        }
        return sum;
    }
    ```
    

### Conclusion

Ending with an extra bit of information about JavaScript functions...

We can exit loop by using both return and break statement.

**Today I learned about While Loop and Break Statement and also practiced a few Questions in JavaScript.**

#### If You ❤️ My Content! Connect Me on [Twitter](https://mobile.twitter.com/Astrodevil_) or Supports Me By [Buying Me A Coffee☕](https://www.buymeacoffee.com/Astrodevil)