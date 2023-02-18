---
title: "JavaScript Fundamentals: Math Object"
date: 2022-12-18T16:52:05+05:30
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
description: "Day 4 of #100DaysOfCode"

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
    image: "https://miro.medium.com/v2/resize:fit:1100/format:webp/1*ul199T8Bd8GhtlgziTWB-w.png" # image path/url
    alt: "Astrodevil" # alt text
    caption: "Photo By Mr. Ånand" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
editPost:
    URL: "https://github.com/Astrodevil/Astrodevil.github.io/tree/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

Today is the 4th day of my **#100DaysOfCode** journey with JavaScript.

I write about my learnings in an explained way through my [blogs](https://astrodevil.hashnode.dev/) and socials. If you want to join me on the learning journey, make sure to follow my blogs and social and share yours too. **Let's learn together!🫱🏼‍🫲🏼**

This Article is a part of the [JavaScript Fundamentals](https://blog.mranand.com/series/js-fundamentals) series.

Today, I learned about `Math.random`, `Math.floor` Functions and to call a function within our function.

### Math.random

In JavaScript, there are many math utilities on the `Math` object. To get a random number we can call the `Math.random` function.

```javascript
const myRandomNumber = Math.random();
```

The above line will return some number between `0` and `1` (not including `1`). `Math.random` can also be used to generate random numbers between the range.

**Example:** Inside `getRandom`, get a random number from the `Math.random()` function. Then, return that number!👇🏼

```javascript
function getRandom() {
    return Math.random();
}
```

A random number between `0` and `100` could be created by simply multiplying the output:

```javascript
// randomNumber will be between 0 and 100
const randomNumber = Math.random() * 100;
```

We could multiply and then add to get a random number between `15` and `100`:

```javascript
// randomNumber will be between 15 and 100
const randomNumber = (Math.random() * 85) + 15;
```

### Math.floor

`Math.floor` takes arguments.

```javascript
const two = Math.floor(2.2598223);
```

`Math.floor` function will take `2.2598223` and return `2`. A number will be rounded to the nearest integer using this function. For instance, if the input was `2.9999`, the method would round it to `2`.

**Example:** Take the argument `x` and use `Math.floor` to turn it into an integer without the values after the decimal place. Once you have this floored value, return it!

```javascript
function getFloor(x) {
    return Math.floor(x);
}
```

### Conclusion

Ending with an extra bit of information about JavaScript functions...

The JavaScript Math object allows us to perform mathematical tasks on numbers. There are various math object properties.

**Today I learned about Math.random, Math.floor Functions in JavaScript.**

#### If You ❤️ My Content! Connect Me on [Twitter](https://mobile.twitter.com/Astrodevil_) or Supports Me By [Buying Me A Coffee☕](https://www.buymeacoffee.com/Astrodevil)