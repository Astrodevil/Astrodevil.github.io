---
title: "JavaScript Fundamentals: Parameters, Arguments and Operators"
date: 2022-12-17T16:52:05+05:30
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
description: "Day 3 of #100DaysOfCode"

# canonicalURL: "https://blog.mranand.com/javascript-fundamentals-parameters-arguments-and-operators"
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
    image: "https://miro.medium.com/v2/resize:fit:1100/format:webp/1*b5xMth2-8W__Qs0mr1V8Ew.png" # image path/url
    alt: "Astrodevil" # alt text
    caption: "Photo By Mr. Ånand" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
editPost:
    URL: "https://github.com/Astrodevil/Astrodevil.github.io/tree/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

Today is the 3rd day of my **#100DaysOfCode** journey with JavaScript.

I write about my learnings in an explained way through my blogs and socials. If you want to join me on the learning journey, make sure to follow my blogs and social and share yours too. **Let's learn together!🫱🏼‍🫲🏼**

This Article is a part of the [JavaScript Fundamentals](https://mranand.com/series/javascript-fundamentals/) series.

I studied functions yesterday, check the previous [article](https://astrodevil.hashnode.dev/javascript-fundamentals-mutable-letcomments-functions). Today it's time to know more about functions and the use of operators.

### **Parameters and Arguments**

Both the terms **parameter** and **argument** refer to the inputs supplied to a function.

Here's a function with two inputs:

```javascript
function addNumbers(a, b) {
    return a + b;
}
```

In the above code, there are two **parameters**: `a` and `b`. These are the variables that are defined in the function declaration.

If we were to call this function with two values: `2` and `4`

```javascript
addNumbers(2, 4);
```

The values `2` and `4` would be considered **arguments**. Arguments are the data supplied to the function to get filled into parameters.

### Operators

JavaScript operators are symbols that are used to perform operations on operands. These are `+`, `-`, `*`, `/` .

`+` **Operator**

The `+` is referred to as an addition operator.

Complete the `addTwo` function to take an input and add `5` to it.

```javascript
function addTwo(input) {
    const output = input + 5;

    return output;
}
```

`*` **Operator**

The `*` is referred to as a multiplication operator.

```javascript
const a = 3;
const b = a * 4;
```

In the above code, `b` will have the value `12`! We are using the multiplication operator to multiply `3` and `4`.

Let's see with multiple inputs👇🏼by putting multiple inputs under `()` separated with `comma`!

```javascript
function product(2,3) {
    return 2*3;
}
```

`/` **Operator**

The `/` is referred to as a division operator.

Find the average of some numbers:

```javascript
const sum = 2 + 7 + 6;
const average = sum / 3;
```

Or we can use parenthesis `()`:

```javascript
const average = (2 + 7 + 6) / 3;
```

In the above code, the sum of `2`, `7`, and `6` is `15`. Then we divide `15` by `3` (`15 / 3`) to get `5`.

The parenthesis will always be evaluated first before any other part of the expression.

### Conclusion

Ending with an extra bit of information about JavaScript functions...

Priority is given to division and multiplication above addition and subtraction. Expressions are evaluated from left to right if the precedence of the operators is the same, as it is when division and multiplication are used.

**Today I learned about Parameters, Arguments and Operators in JavaScript.**

#### If You ❤️ My Content! Connect Me on [Twitter](https://mobile.twitter.com/Astrodevil_) or Supports Me By [Buying Me A Coffee☕](https://www.buymeacoffee.com/Astrodevil)