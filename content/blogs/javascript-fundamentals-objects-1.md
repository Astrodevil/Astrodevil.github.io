---
title: "JavaScript Fundamentals: Objects 1"
date: 2023-01-03T16:52:05+05:30
draft: false

# weight: 2
# aliases: ["/first"]
tags: ["javascript", "tutorial", "webdevelopment", "100daysofcode", "programming", "coding"]
author: "Mr. Ånand"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "Day 13 of #100DaysOfCode"

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
    image: "https://blog.mranand.com/_next/image?url=https%3A%2F%2Fcdn.hashnode.com%2Fres%2Fhashnode%2Fimage%2Fupload%2Fv1672761290549%2F9c641241-f603-4eed-beb5-a6ef732b090a.png%3Fw%3D1600%26h%3D840%26fit%3Dcrop%26crop%3Dentropy%26auto%3Dcompress%2Cformat%26format%3Dwebp&w=3840&q=75" # image path/url
    alt: "Astrodevil" # alt text
    caption: "Photo By Mr. Ånand" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
   # URL: "https://github.com/<path_to_repo>/content"
   # Text: "Suggest Changes" # edit text
   # appendFilePath: true # to append file path to Edit link
---

Today is the 13th day of my **#100DaysOfCode** journey with JavaScript.

I write about my learnings in an explained way through my [blogs](https://astrodevil.hashnode.dev/) and socials. If you want to join me on the learning journey, make sure to follow my blogs and social and share yours too. **Let's learn together!🫱🏼‍🫲🏼**

This Article is a part of the [JavaScript Fundamentals](https://blog.mranand.com/series/js-fundamentals) series.

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

### Conclusion

Ending with an extra bit of information about JavaScript...

A JavaScript object is a state-and-behaviour-containing entity (properties and method). Examples include a car, pen, bicycle, chair, glass, keyboard, and monitor. JavaScript is an object-based language. In JavaScript, everything is an object. JavaScript relies on templates rather than classes. To obtain the object in this case, no class is created. But we deliberately make objects.

**Today I learned about Objects in JavaScript.**

#### If You ❤️ My Content! Connect Me on [Twitter](https://mobile.twitter.com/Astrodevil_) or Supports Me By [Buying Me A Coffee☕](https://www.buymeacoffee.com/Astrodevil)