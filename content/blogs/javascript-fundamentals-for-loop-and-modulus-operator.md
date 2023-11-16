---
title: "JavaScript Fundamentals: For Loop and Modulus Operator"
date: 2022-12-21T16:52:05+05:30
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
description: "Day 6 of #100DaysOfCode"

# canonicalURL: "https://blog.mranand.com/javascript-fundamentals-math-object"
disableHLJS: false # to enable highlightjs
disableShare: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowWordCount: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowShareButtons: true
cover:
    image: "https://miro.medium.com/v2/resize:fit:1100/format:webp/1*UJKxubY2QVy28PhhQu4pRg.png" # image path/url
    alt: "Astrodevil" # alt text
    caption: "Photo By Mr. Ånand" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
editPost:
    URL: "https://github.com/Astrodevil/Astrodevil.github.io/tree/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

Today is the 6th day of my **#100DaysOfCode** journey with JavaScript.

I write about my learnings in an explained way through my blogs and socials. If you want to join me on the learning journey, make sure to follow my blogs and social and share yours too. **Let's learn together!🫱🏼‍🫲🏼**

This Article is a part of the [JavaScript Fundamentals](https://mranand.com/series/javascript-fundamentals/) series.

### Loops

Loops provide a quick and simple way to repeat an action. Programmers take advantage of this speed by creating scripts that do a task repeatedly until a predetermined condition is satisfied.

In *pseudocode* this might look a little like this:

```javascript
while we have book
    read book
    while we have pages in this book
        read page
            while we have words on the page
                read word 
```

### For Loop

A `for` loop repeats until a specified condition evaluates to false.

*   **Summation** of numbers example:
    

Let's think about how to repeatedly add the digits 1, 2, 3, and 4: The first step is to add 1 to a sum. Then we go to 2, add this to the total, and so on until we get to 4. An iteration occurs each time we add to the total. When the value is more than 4, we iterate until we reach our exit condition.

```javascript
let sum = 0;
for(let i = 1; i <= 4; i++) { 
    sum = sum + i; 
}
```

The `for` loop can be broken down into the *initialization*, *condition*, *update* and *statement*: Compare 👇🏼with👆🏼

```plaintext
for ([initialization]; [condition]; [update]) {
    statement
}
```

The **Initialization** is run once at the beginning of the loop. The **Condition** is checked before each iteration. The **Update** is run at the end of each iteration. The **Statement** is run as long as the Condition is true.

*   **Factorial** of numbers example:
    

In mathematics, a factorial is often denoted with an exclamation mark `!`. The sum of all positive integers greater than 0 up to and including the factorial number `n` is known as a factorial.

Let's take a look at a few examples of factorials:

`4! = 4 * 3 * 2 * 1 = 24`

`3! = 3 * 2 * 1 = 6`

`2! = 2 * 1 = 2`  

**Example:** Taking in some integer value `n`, find the factorial for that number and return it.

```javascript
function factorial(n){
let result = 1;
for (let i = 1; i <= n; i++){
result = result * i; // or result *= i;
}
return result;
}
```

*   **Strings** in loops example:
    

Let's add some exclamation marks to `"Hello World"`!

```javascript
let str = "Hello World";
for(let i = 1; i <= 3; i++) {
    str += "!";
}
console.log(str); // Hello World!!!
```

**Example:** Let's create a function `scream` which will take in a value `n` and return a string with the letter "`a`" repeated that many times like `scream(5); // "aaaaa"`

```javascript
function scream(n) {
    let str = "";
    let i = 1;
    for (let i = 1; i<=n; i++){
        str += "a"
        }
    return str;
}
```

### Modulus Operator

`%` operator is called the modulus operator. It will tell us the remainder of a division. When you divide `9` by `2` you get. Or `4` with a remainder of `1`. The expression `9` % `2` evaluates to that remainder: `1`

Let's take a look at a few examples:

```javascript
console.log(8 % 3) // 2
console.log(9 % 2) // 1
console.log(7 % 4) // 3
```

**Example:** Let's modify our function to return a scream alternating between lower and capital case, like these:

`console.log( scream(4) ); // aAaA console.log( scream(9) ); // aAaAaAaAa`

```javascript
function scream(n) {
    let str = "";
   
    for (let i = 1; i <= n; i++) {
        const remainder = i % 2;
        const isEven = remainder === 0;
        if (isEven) {
            str += "A";
        }
        else {
            str += "a";
    }
}
    return str;
}
```

### Conclusion

Ending with an extra bit of information about JavaScript functions...

At the beginning of the `for` loop, the **Initialization** is once executed. Each iteration begins with a check of the **Condition**. The **Statement** will be executed if the expression evaluates to true. If it's untrue, the statement won't execute. Each iteration ends with the **Update** being executed. For the subsequent execution of the **Statement**, it may update a variable. As long as the **Condition** is true, the **Statement** is then executed. The actual work of the loop is completed here.

**Today I learned about For Loop, Modulus Operator in JavaScript.**

#### If You ❤️ My Content! Connect Me on [Twitter](https://mobile.twitter.com/Astrodevil_) 
{{< bmc-button slug="Astrodevil">}}