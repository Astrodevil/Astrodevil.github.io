---
title: "JavaScript Fundamentals: String Looping, Index Of and Slicing Strings"
date: 2022-12-25T16:52:05+05:30
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
description: "Day 9 of #100DaysOfCode"

# canonicalURL: "https://blog.mranand.com/javascript-fundamentals-math-object"
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
    image: "https://miro.medium.com/v2/resize:fit:1100/0*eHuv8IO_n6zHKFt4" # image path/url
    alt: "Astrodevil" # alt text
    caption: "Photo By Mr. Ånand" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
editPost:
    URL: "https://github.com/Astrodevil/Astrodevil.github.io/tree/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

Today is the 9th day of my **#100DaysOfCode** journey with JavaScript.

I write about my learnings in an explained way through my blogs and socials. If you want to join me on the learning journey, make sure to follow my blogs and social and share yours too. **Let's learn together!🫱🏼‍🫲🏼**

This Article is a part of the [JavaScript Fundamentals](https://mranand.com/series/javascript-fundamentals/) series.

### String Looping

Strings are really simple to loop through. We learned how to retrieve characters by using the `.length` property and `[]`.

So how can we loop over strings using these?

```javascript
const string = "Hello";
for(let i = 0; i < string.length; i++) {
    console.log(string[i]);
}
```

It will log: `H`, `e`, `l`, `l`, `o` in that order after each iteration.

**Example:** Complete the function `isAllX` to determine if the **entire string** is made of lower-case `x` or upper-case `X`. Return `true` if they are, `false` if not.

```javascript
function isAllX(string) {
for(let i = 0; i < string.length; i++){
    if(string[i].toLowerCase() !== "x"){
        return false;
    }
}
return true;
}
```

### Index Of

In the previous section, we learned to look up a character by `index`. Now, is the time to find the `index` of a specific string.

`indexOf` method is used to find the **first** index of a string.

```javascript
"Hello".indexOf("e"); // 1
"abc".indexOf("q"); // -1 
"happy man dance".indexOf("man"); // 6
```

Both single characters and entire strings can be searched for in the index! `indexOf` will return `-1` if the index could not be located.

**Example:** In the `string` argument find the index of the first lowercase "x" and return it.

```javascript
function findFirstX(string) {
    return string.indexOf('x');
}
```

### Slicing Strings

We have another string method **slice!**

Slice accepts two parameters: a **start** index and an **end** index. The resulting string is a sliced string between those two indexes, except for the character at the **end** index.

```javascript
"An apple".slice(0,2); // An
"The 20 Jokers".slice(4,8); // 20 J
```

If the last index is not provided, slice will continue until the end of the string:

```javascript
"Please Slice Me".slice(7); // Slice Me
```

We can also use **negative arguments** to slice strings **starting from the end** of the string!

```javascript
"the apple".slice(-5); // apple
"the apple".slice(-5, -1); // appl
```

**Example:** Let's find the longer half of the string before and after the `x`! First, you'll need to find the **lower-case** `x`. Once you've found the `x`, split the string in half. The first half will be the string before the `x`, the second half will be the string after the `x`.

Take the **longer** string and return it!

```javascript
// split the string at the first occurrence of x
// return the larger of the two resulting strings
// i.e. HappyxDeveloper => Developer
function splitAtX(string) {
    const index = string.indexOf('x');
    const a = string.slice(0,index);
    const b = string.slice(index+1);
    return (a.length > b.length) ? a : b;
}
```

### Conclusion

Ending with an extra bit of information about JavaScript functions...

On strings, there is a `lastIndexOf` method as well. It locates the string's last occurrence and returns its index.

**Today I learned about String Looping, Index Of and Slicing Strings in JavaScript.**

#### If You ❤️ My Content! Connect Me on [Twitter](https://mobile.twitter.com/Astrodevil_) or Supports Me By [Buying Me A Coffee☕](https://www.buymeacoffee.com/Astrodevil)