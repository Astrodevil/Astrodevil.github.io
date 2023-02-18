---
title: "JavaScript Fundamentals: Conditionals"
date: 2022-12-19T16:52:05+05:30
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
description: "Day 5 of #100DaysOfCode"

# canonicalURL: "https://blog.mranand.com/javascript-fundamentals-math-object"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: false
ShowWordCount: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowShareButtons: true
cover:
    image: "https://miro.medium.com/v2/resize:fit:1100/format:webp/1*rY5Y8Wys8rsrtoyoOGuRLg.png" # image path/url
    alt: "Astrodevil" # alt text
    caption: "Photo By Mr. Ånand" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
editPost:
    URL: "https://github.com/Astrodevil/Astrodevil.github.io/tree/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

Today is the 5th day of my **#100DaysOfCode** journey with JavaScript.

I write about my learnings in an explained way through my [blogs](https://astrodevil.hashnode.dev/) and socials. If you want to join me on the learning journey, make sure to follow my blogs and social and share yours too. **Let's learn together!🫱🏼‍🫲🏼**

This Article is a part of the [JavaScript Fundamentals](https://astrodevil.hashnode.dev/series/js-fundamentals) series.

### Console Log

The `console.log` will log values during the program's execution. If we `console.log` a value, that value will show in our test results. You will also often see `console.log` used in code examples:

```javascript
let a = 22; 
a = a + 10; 
console.log(a); // 32;
```

### Conditionals

Conditional statements control behaviour in JavaScript and determine whether or not pieces of code can run.

*   `if` **Statement**
    
    Use of `if` when needing to branch based on a **condition**:
    
    ```javascript
    if(1 === 1) {
        console.log( "Yes, it's true!" );
    }
    ```
    
    In the above line, `1 === 1` is the condition. The `===` operator referred to as the strict **equality** operator. It compares two values and evaluates them to be `true` if they are equal.
    
    **Example:** Let's complete the isEqual function! If a is equal to b return true.
    
    ```javascript
    function isEqual(a, b) {
        return(a===b);
    }
    ```
    
    `!==` or **Is Not Equal** referred to as **a strict inequality** operator. This operator will evaluate to `true` if the two values are not equal.
    
    ```javascript
    console.log( 1 !== 2 ); // true
    console.log( 2 !== 2 ); // false
    console.log( 3 !== 2 ); // true
    ```
    
    **Example:** Let's complete the `isNotEqual` function! If `a` is **not equal** to `b` return `true`.
    
    ```javascript
    function isNotEqual(a, b) {
        if(a !== b){
            return true;
        }
    }
    ```
    
*   `else` **Statement**
    
    The `else` statement runs only if the `if` condition is **not true**.
    
    ```javascript
    if(isRaining === true) {
        stayIndoors();
    }
    else {
        // isRaining is not true
        goOutside();
    }
    ```
    
    **Example:** Let's update our `isNotEqual` function to also handle the case where `a` is equal to `b`. If a is not equal to `b` return true. Otherwise, return `false`.
    
    ```javascript
    function greater(first, last) {
        if (first > last){
            return first;
        }
        if (last > first) {
            return last;
        }
    }
    ```
    
    Let's take a look at two new operators, greater than `>` and less than `<` operators! Both `>` and `<` will evaluate to `false` if the **operands** are **equal**:
    
    ```javascript
    console.log(1 > 3); // false
    console.log(3 > 1); // true
    
    console.log(3 < 1); // false
    console.log(1 < 3); // true
    ```
    
    The values on either side of the operator are referred to as "**operands**". The operands for the equation `1 > 3` are `1` and `3`.
    
*   `>=` or `<=` **Operator**
    
    Both `>=` and `<=` will evaluate to `true` when the **operands** are equal, unlike the `>` and `<` operators.
    
    ```javascript
    function greaterThanOrEqualTo(a, b) {
        if(a > b) {
            return true;
        }
        if(a === b) {
            return true;
        }
    }
    
    // or
    // Both will accomplish the same functionality.
    
    function isEqual(a,b) {
        if(a === b) {
            return true;
        }
        return false;
    }
    ```
    
*   `else If` **Statement**
    
    We can use `else` and `if` together:
    
    ```javascript
    if(firstCondition) {
        // firstCondition is true
    }
    else if (otherCondition) {
        // firstCondition is not true and otherCondition is true
    }
    else {
        // neither condition is true
    }
    ```
    
    What happens if the two conditions were `true`?
    
    ```javascript
    const a = true;
    const b = true;
    
    if(a) {
        // this will run
    }
    else if (b) {
        // this will not run!
    }
    else {
        // this will definitely not run.
    }
    ```
    
    The important thing to take away from this is that `else` statements will only run if the original condition is not `true`.
    

### Conclusion

Ending with an extra bit of information about JavaScript...

In order to guarantee that code is readable to a standard, many organisations maintain a rigid style guide. `{}` are typically recommended for `if/else` statements.

**Today I learned about Conditionals, If, Else, Else If in JavaScript.**

#### If You ❤️ My Content! Connect Me on [Twitter](https://mobile.twitter.com/Astrodevil_) or Supports Me By [Buying Me A Coffee☕](https://www.buymeacoffee.com/Astrodevil)