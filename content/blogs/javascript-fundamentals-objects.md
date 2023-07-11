---
title: "JavaScript Fundamentals: Objects"
date: 2023-01-03T16:52:05+05:30
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
description: "Day 13 of #100DaysOfCode"

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
    image: "https://miro.medium.com/v2/resize:fit:1100/0*vc8NwJJmC4v-3g8S" # image path/url
    alt: "Astrodevil" # alt text
    caption: "Photo By Mr. Ånand" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
editPost:
    URL: "https://github.com/Astrodevil/Astrodevil.github.io/tree/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

Today is the 13th day of my **#100DaysOfCode** journey with JavaScript.

I write about my learnings in an explained way through my blogs and socials. If you want to join me on the learning journey, make sure to follow my blogs and social and share yours too. **Let's learn together!🫱🏼‍🫲🏼**

This Article is a part of the [JavaScript Fundamentals](https://mranand.com/series/javascript-fundamentals/) series.

### Objects

In JavaScript, almost "everything" is an object. JavaScript objects start with an open curly-brace `{` and end with a closed curly brace `}`. It contains key-value pairs in between these braces.

```javascript
const team = {
    name: "India",
    wins: 91,
    inFinals: true,
};
```

In above object `team`, we have three keys: `name`, `wins` and `inFinals`. The value associated with `name` is `"India"`, with `wins` is `86` and with `inFinals` is `true`.

**Example:** Let's create an object representing a pizza order! In the `order` object, add the following three keys with values accordingly:

`pizzas` - Any number greater than zero.

`extraCheese` - A boolean. Either `true` or `false`.

`deliveryInstructions` - Any string of instructions.

```javascript
const order = {
    pizzas: 5,
    extraCheese: true,
    deliveryInstructions: "Keep it medium",
};
```

### Retrieve Values

Now we will retrieve values from object. From the given code, If we wanted to retrieve the name of the team, we can do this in two ways:

```javascript
const team = {
    name: "India",
    wins: 91,
    inFinals: true,
};
```

```javascript
console.log( team.name ); // India
console.log( team['name'] ); // India
```

Brackets `[]` or `.` property accessor operator can be used, similar to arrays!

### Array of Objects

Now, we will see what happens if we put objects inside arrays and vice versa.

Let's take our team example again:

```javascript
const team = {
    name: "India",
    wins: 91,
    inFinals: true,
};
```

What if we have multiple teams:

```javascript
const teams = [India, Australia, England];
for(let i = 0; i < teams.length; i++) {
    console.log(teams[i].name); 
}
```

This example loops over each team and logs out the name of each team.

**Example:** Given an array of pizza orders, return the total number of pizzas ordered. The `orders` are an array of objects, each with `pizzas` key inside.

```javascript
function numberOfPizzas(orders) {
    let total = 0;
    for(let i = 0; i < orders.length; i++) {
        total += orders[i].pizzas;
    }
    return total;
}
```

### Enumerated Types

When numbers are defined, code is easier to read and maintain. Consider the following instance:

```javascript
const card = {
    suit: 1,
    value: 5
}
```

Spades, Clubs, Hearts, and Diamond cards are suits.

What is the `suit` of this card? We are aware that the value is `1`, but what does that actually mean? Let's define `CARD_SUITS`:

```javascript
const CARD_SUITS = {
    DIAMONDS: 0,
    HEARTS: 1,
    SPADES: 2,
    CLUBS: 3
}
```

We can identify our card `suit` by using this object:

```javascript
const card = {
    suit: CARD_SUITS.HEARTS,
    value: 5
}
```

It only needs to be changed once in `CARD_SUITS` if we ever wish to change which suit belongs to which value. This type of object is commonly referred to as an Enumeration.

**Example:** Let's create an enumeration like `CARD_SUITS` above. Our enumeration will be named `ORDER_TYPES` and describe the different types of orders that are possible in our system. The first type should be `PIZZA,` with a value of `0`. After that, create at least 2 more options of your choice!

```javascript
const ORDER_TYPES = {
    PIZZA: 0,
    WINGS: 1,
    SALAD: 2,
}
```

### Importing Files

Let's import the `ORDER_TYPES` we just created into `numberOfPizzas.js`.

We can use `require` to pull in the exports from `orderType.js`:

```javascript
const ORDER_TYPES = require('./orderTypes');
```

**Example:** Modify the `numberOfPizzas` function to only count pizzas when the `order.type` is equal to `ORDER_TYPES.PIZZA`.

```javascript
// orderTypes.js

const ORDER_TYPES = {
    PIZZA: 0,
    WINGS: 1,
    SALAD: 2,
}
```

```javascript
// numberOfPizzas.js

const ORDER_TYPES = require('./orderTypes');

function numberOfPizzas(orders) {
    let total = 0;
    for(let i = 0; i < orders.length; i++) {
        if (orders[i].type === ORDER_TYPES.PIZZA) {
            total += orders[i].pizzas;
        }
    }
    return total;
}
```

### Number of Keys

There are a few approaches to obtaining every key in an object. To iterate across all properties, we can use the `in` operator:

```javascript
const object = { a: 1, b: 2, c: 3 } 
for(let key in object) {
    console.log(key);
}
```

After 3 iterations this will log `a`, `b` and `c` which are the keys of `object`. We can use some methods on `object` that will return an array of that data.

```javascript
const object = { a: 1, b: 2, c: 3 } 
console.log( Object.keys(object) ); // ['a', 'b', 'c']
console.log( Object.values(object) ); // [1, 2, 3]
```

**Example:** Given an object, find the number of keys inside the object. Return this number.

```javascript
function numberOfKeys(object) {
    return Object.keys(object).length;
}
```

### Edit Object Values

We can also edit values in an object.

```javascript
const person = {
    name: "Sohan",
    age: 21
}

person.name = "Rohan";
person["age"] = 40;

console.log( person.name ); // Rohan
console.log( person.age ); // 40
```

In retrieval, we can use the `.` or `[]` notation. We can also remove keys completly.

```javascript
const person = { 
    name: "Tom"
}

delete person.name;

console.log( person.name ); // undefined
```

### Modify Object

In JavaScript, objects are passed by reference. We can write functions to modify objects.

```javascript
function modify(object) {
    object.message = "Hello World";
}
```

Let's create an object and pass it to the above function:

```javascript
const store = {
    name: "Star Eleven" 
}

modify(store);

console.log(store.message); // Hello World
```

The `object` argument within the `modify` method is referencing the same memory as the `store`. Passing by reference is defined as this.

The `object` gets updated everywhere it is referenced when it is updated using the `modify` function.

### Conclusion

Ending with an extra bit of information about JavaScript...

A JavaScript object is a state-and-behaviour-containing entity (properties and method). Examples include a car, pen, bicycle, chair, glass, keyboard, and monitor. JavaScript is an object-based language. In JavaScript, everything is an object. JavaScript relies on templates rather than classes. To obtain the object in this case, no class is created. But we deliberately make objects.

It is always a good idea to be careful about modifying objects directly! The function is modifying something outside of its scope, potentially leading to unexpected consequences!

**Today I learned about Objects in JavaScript.**

#### If You ❤️ My Content! Connect Me on [Twitter](https://mobile.twitter.com/Astrodevil_) 

{{< bmc-button slug="Astrodevil">}}