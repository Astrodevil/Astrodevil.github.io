---
title: "JavaScript Fundamentals: Number Variable, Multiple Variables, Booleans, Strings"
date: 2022-12-15T16:52:05+05:30
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
description: "Day 1 of #100DaysOfCode"

# canonicalURL: "https://blog.mranand.com/javascript-fundamentals-number-variable-multiple-variables-booleans-strings"
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
    image: "https://miro.medium.com/v2/resize:fit:1100/format:webp/1*NUoqOLLiHpD0M1LBsxXlaA.png" # image path/url
    alt: "Astrodevil" # alt text
    caption: "Photo By Mr. Ånand" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
editPost:
    URL: "https://github.com/Astrodevil/Astrodevil.github.io/tree/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

After exams and lots of procrastination, I finally resumed my **#100DaysOfCode** journey with JavaScript. Today is the 1st day of my journey and learned some basic concepts of JavaScript.

I am going to write about my learnings in an explained way through my blogs and socials. If you want to join me on the learning journey, make sure to follow my blogs and social and share yours too. **Let's learn together!🫱🏼‍🫲🏼**

### Introduction to JavaScript

The foundation of contemporary online apps is JavaScript. Although that may sound pretentious or flowery, it is also the reality. JavaScript powers the contemporary web, your contemporary servers, and even the development environments on our computers. Whether it is web 2.0 or web 3.0, JavaScript is used everywhere.

### Number Variable

A JavaScript variable is nothing more than a name for a storage area. In JavaScript, there are two different sorts of variables: local variables and global variables. When declaring a JavaScript variable, there are several guidelines (also known as identifiers).

*   The name must begin with an alphabetical letter (from A to Z), an underscore (\_), or a dollar sign ($).
    
*   The first letter can be followed by any number from 0 to 9, such as the value 1.
    
*   JavaScript variables are case-sensitive; for instance, the variables x and X are distinct.
    
*   JavaScript variables are written in **lowerCamelCase.** for example `const isLoggedIn = true;`
    
*   JavaScript cares about variables in one word (not separated by space).
    

We store values in something called a variable.

`const a = 5`

In the above code, `a` is the variable. Number `5` is the value to be stored in `a` and `const` is a keyword used to declare `a` as a constant value in JavaScript.

### Multiple Variables

JavaScript programs run line by line, the line `const a = 5` is called a statement. In JavaScript, statements should end with `;` (semi-colon). In some cases, JavaScript automatically inserts semi-colons in a statement. The best practice is to insert `;` at every statement end.

We can create another variable to store the value of the previous variable.

`const a = 5;`

`const b = a;`

Both `a` and `b` will store the value `5`.

### Booleans

A JavaScript Boolean represents one of two values: **true** or **false**.

`const loggedIn = false;`

If a user is logged in the above line, the `false` indicated that they are not.

We can also store boolean values inside variables. If we have to store `true` in one variable and `false` in another variable, then:

`cont a = false;`

`const b = true;`

### Quotes

Both single `' '` and double `" "` quotes can be used when declaring JavaScript strings.

Here, we used double quotes so we could use a single quote inside the message:

`const message = "Hello, hope you are doing fine!" ;`

If we needed to use double quotes:

`const message = 'Then he said, "Hey, are you coming home?"';`

If we needed to use a double quote inside double quote string, we can use a backslash `\` as an escape character:

`const message = "This is double-quote \" inside double-quotes";`

### Strings

Strings in JavaScript are used to store and modify text. A string in JavaScript is zero or more characters enclosed in quotes.

Strings are nothing but a bunch of characters (`a`, `b`, `c`) put together.

In JavaScript, there are three ways to define a string. first two of them are:

*   `const a = "Hello!";`
    
*   Here, `myName` and `anotherName` uses two different types of quotes, single and double. We can use either one or inside of each other.
    
    `const myName = 'Anand';`
    
    `const anotherName = "Vishal";`
    

Now look at the third method to declare strings:

``const helloMessage = `Hello ${myName}, my name is ${anothername}!`;``

Here, `helloMessage` variable uses backticks `` ` `` . With backticks, we can add values inside the strings. The `${variable}` is about this. In the above line of code, we are taking value from `myName` and `anotherName` and placing them into strings. The variable `helloMessage` now contains `"Hello Anand, my name is Vishal!"`

### Conclusion

Ending with an extra bit of information about JavaScript...

JavaScript also uses **upper snake case** sometimes like `const SERVER_KEY_VALUE = "abcdefg";` This casing is typically reserved for environment variables or values that are needed to be determined before code executions. Like, if you have some secret key that you want to store on the server but not on the local machine, then You might keep that variable tucked away on the server in an environment variable that will require permissions to access or change. These are the types of variables we'll often see with this casing.

**Today I learned about Number variables, multiple variables, booleans, quotes and strings in JavaScript.**

#### If You ❤️ My Content! Connect Me on [Twitter](https://mobile.twitter.com/Astrodevil_) 

{{< bmc-button slug="Astrodevil">}}
