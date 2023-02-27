---
title: "JavaScript Fundamentals: Mutable let,Comments, Functions"
date: 2022-12-16T16:52:05+05:30
draft: false

series: [JavaScript Fundamentals]
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
description: "Day 2 of #100DaysOfCode"

# canonicalURL: "https://blog.mranand.com/javascript-fundamentals-mutable-letcomments-functions"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowWordCount: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowShareButtons: true
cover:
    image: "https://miro.medium.com/v2/resize:fit:1100/format:webp/1*0AlaWdc8ZDsKrqwI-ypK8g.png" # image path/url
    alt: "Astrodevil" # alt text
    caption: "Photo By Mr. Ånand" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
editPost:
    URL: "https://github.com/Astrodevil/Astrodevil.github.io/tree/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

Today is the 2nd day of my **#100DaysOfCode** journey with JavaScript.

I am going to write about my learnings in an explained way through my blogs and socials. If you want to join me on the learning journey, make sure to follow my blogs and social and share yours too. **Let's learn together!🫱🏼‍🫲🏼**

This Article is a part of the [JavaScript Fundamentals](https://mranand.com/series/javascript-fundamentals/) series.

### Mutable let

We worked on variables in the last section and now going further with variables, how can we change the stored value inside of a variable?

We used `const` keyword to declare a constant variable, but if we try to change the value it will give errors.

```javascript
const a = 4;
a = 8;
```

If we try to run above the line, it will give `TypeError: Assignment to constant variable` . Constants are immutable, meaning their value cannot change.

Here comes the keyword `let` which allows the value to be mutable (meaning it can change).

```javascript
let a = 4;
a = 8;
```

The above line will run without error.

### Comments

Comments are an important part of programs. Writing good comments is also necessary to be a good programmer and to write clean code.

Coming up with good variable names is also important.

```javascript
const value = 99;
const price = 99;
```

Both hold the same value `99` but `price` is more descriptive.

Comments are only for humans to understand code in a better way. We can write single-line or multi-line comments.

```javascript
// this is price in U.S. Dollars
const price = 99;
```

```javascript
/* The price of all items
   Denominated in U.S. Dollars  */
const price = 99;
```

### Functions

A function is a reusable code and it returns an output. The function must be defined before calling it. Function call means to execute the function. The word *invoke* is also used and the meaning is the same as call.

When a function is called, It means you're passing specific input values.

```javascript
const output = addOne(5);
```

In the code above, `addOne` is the function and parenthesis `( )` is used to call the function. We are passing in an input value 5 into our function addOne.

It is not mandatory to have input values in the function. See the below example.

```javascript
const message = getMessage();
```

In order to call a function, we must first define it!

```javascript
function addOne(input) {
    return input + 2;
}
```

In the above code, we are creating a function called `addOne` which takes one input called input. We are returning the input plus two.

```javascript
function getMessage() {
    return "Hello World!";
}
```

In the above code, function `getMessage` does not take input. We are simply returning a string, saying "Hello World!". The `return` statement will return the desired output of the function.

```javascript
const a = addOne(2);
```

Variable `a` is now assigned to the return value of the `addOne` function invoked with an input of 2, which evaluates to 4.

### Conclusion

Ending with an extra bit of information about JavaScript functions...

If we define/declare a function once, it can be called elsewhere in the program.

**Today I learned about Mutable let, Comments, and Functions in JavaScript.**

#### If You ❤️ My Content! Connect Me on [Twitter](https://mobile.twitter.com/Astrodevil_) or Supports Me By [Buying Me A Coffee☕](https://www.buymeacoffee.com/Astrodevil)