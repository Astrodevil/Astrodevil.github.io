---
title: "JavaScript Fundamentals: String Manipulation"
date: 2022-12-23T16:52:05+05:30
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
description: "Day 8 of #100DaysOfCode"

# canonicalURL: "https://blog.mranand.com/javascript-fundamentals-math-object"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowShareButtons: true
cover:
    image: "https://blog.mranand.com/_next/image?url=https%3A%2F%2Fcdn.hashnode.com%2Fres%2Fhashnode%2Fimage%2Fupload%2Fv1671814005049%2F7fd581b7-e9ef-4f6c-a811-a27b57cd4255.png%3Fw%3D1600%26h%3D840%26fit%3Dcrop%26crop%3Dentropy%26auto%3Dcompress%2Cformat%26format%3Dwebp&w=3840&q=75" # image path/url
    alt: "Astrodevil" # alt text
    caption: "Photo By Mr. Ånand" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
editPost:
    URL: "https://github.com/Astrodevil/Astrodevil.github.io/tree/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

Today is the 8th day of my **#100DaysOfCode** journey with JavaScript.

I write about my learnings in an explained way through my [blogs](https://astrodevil.hashnode.dev/) and socials. If you want to join me on the learning journey, make sure to follow my blogs and social and share yours too. **Let's learn together!🫱🏼‍🫲🏼**

This Article is a part of the [JavaScript Fundamentals](https://astrodevil.hashnode.dev/series/js-fundamentals) series.

### Comparing Strings

String comparison is actually very simple! The comparison operators `===`, `<` and `>` that we studied in earlier lectures can be used.

For `===`, we may compare the strings case-sensitively to see if they are identical:

```javascript
console.log( 'a' === 'a' ); // true
console.log( 'a' === 'A' ); // false
console.log( 'a' === 'a ' ); // false ------Because the comparison is case-sensitive and requires exact equality, including whitespace.
```

### Looking up Characters

Characters in strings can be looked up by index in JavaScript. Square brackets `[]` or `charAt` are the two methods available for doing this.

```javascript
"Hello".charAt(1); // e
"Hello"[1]; // e

// we are looking up the character at the 1 index, which turns out to be the character e.
```

Indexing:

`H - 0`

`e - 1`

`l - 2`

`l - 3`

`o - 4`

Zero-based indexing is used for strings. This indicates that the index of the first character is `0`, and it increases by 1 for each additional character.

**Example:** Complete the `startsWithX` function to determine if the first character of the `string` argument is the lower-case `x`. If the first character is `x` return `true`. If not, return `false`.

```javascript
function startsWithX(string) {
    if(string[0] === "x") {
        return true;
    }
    return false;
}
```

### Character Casing

When working with strings, we frequently prefer to ignore the character casing. Whether it is an upper-case "X" or lower-case "x," we are looking for "x".

Manipulating a string's case can be done in two simple ways:

```javascript
console.log( "Hello".toLowerCase() );// hello
console.log( "Hello".toUpperCase() ); // HELLO
```

Either of the following can be used to determine whether a string included the word `"hello"` regardless of its case:

```javascript
console.log( "Hello".toUpperCase() === "HELLO" ); // true
console.log( "Hello".toLowerCase() === "hello" ); // true
```

**Example:** Let's update our `startsWithX`(from previous example) function to return `true` for an upper-case `X` as well as a lower-case `x`.

```javascript
function startsWithX(string) {
    if(string[0].toLowerCase() === "x") {
        return true;
    }
    return false;
}
```

### String Length

Strings have an important feature called length. By using this feature, we can quickly determine how many characters are contained in a string:

```javascript
console.log( "a".length ); // 1
console.log( "Hello".length ); // 5
```

**Example:** Complete the `endsWithX` function by detecting if the last character in the string is a lower-case `x` or an upper-case `X`. Return `true` if it is, `false` if not.

Note: The length value will be 1 greater than the last character index because the character indexing is 0 based.

```javascript
function endsWithX(string) {
    if(string[string.length - 1].toLowerCase() === "x") {
        return true;
    }
    return false;
}
```

### Conclusion

Ending with an extra bit of information about JavaScript functions...

Strings in JavaScript allow us to store text that includes characters, integers, and Unicode and is immutable. Additionally, there are numerous built-in functions in JavaScript for creating and manipulating strings in different ways.

**Today I learned about String Manipulation in JavaScript.**

#### If You ❤️ My Content! Connect Me on [Twitter](https://mobile.twitter.com/Astrodevil_) or Supports Me By [Buying Me A Coffee☕](https://www.buymeacoffee.com/Astrodevil)