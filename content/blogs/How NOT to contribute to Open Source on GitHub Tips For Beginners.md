---
title: "How NOT to contribute to Open Source on GitHub: Tips For Beginners"
date: 2022-01-01T17:29:05+05:30
draft: false

# weight: 2
# aliases: ["/first"]
tags: ["github", "opensource", "tutorial"]
author: "Mr. Ånand"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: true
draft: false
hidemeta: false
comments: true
description: "While maintaining some projects on GitHub during Hacktoberfest 2021, I came across many new open source contributors. They are just starting their open-source journey and making mistakes. In the beginning, making mistakes is not a bad thing. But, correctly contributing to open-source projects is also very important.

In this article, I am going to discuss some tips on - How Not to contribute to Open-Source on GitHub."

# canonicalURL: "https://astrodevil.hashnode.dev/how-not-to-contribute-to-open-source-on-github-tips-for-beginners"
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
    image: "https://miro.medium.com/v2/resize:fit:1100/format:webp/1*G_OM24K1jKIp5iYmR5Cd-Q.png" # image path/url
    alt: "Astrodevil" # alt text
    caption: "Photo By Mr. Ånand" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
editPost:
    URL: "https://github.com/Astrodevil/Astrodevil.github.io/tree/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

While maintaining some projects on GitHub during Hacktoberfest 2021, I came across many new open source contributors. They are just starting their open-source journey and making mistakes. In the beginning, making mistakes is not a bad thing. But, correctly contributing to open-source projects is also very important.

In this article, I am going to discuss some tips on - **How Not to contribute to Open-Source on GitHub**.

## Understanding Projects
Understanding of project like how folders are arranged? how files are linked? which tech stack is used? is the most important thing before raising an issue or making a pull request in any project on GitHub. 

**Don't** make pull requests or raise issues without reading contributing guidelines of any projects. Always read the [README.md](https://github.com/ZeroOctave/ZeroOctave-Javascript-Projects/blob/main/README.md) file of projects where everything related to the project is written most of the time. Also, clone the project in your machine and go through every file once to understand its working.

## Raising Issue
If you want to solve any bug or to contribute some lines of code to a project then you have to raise an issue. But always check the previous issues raised by anyone else to confirm, if anyone else is working or described the same issue that you gonna solve. 

**Don't** raise 1 or 2-word issue, that doesn't make sense to anyone else. Always remember to add proper details/context in the issue because the issue is like a chain of conversation related to changes you or anyone else wants to make in the project. Write a proper description and proper title to the issue also add screenshots, links, information, or an approach to solve that issue to proper understanding. Make issues such that project maintainers or contributors understand your views and suggestions quickly.

✅**Do this**
![Screenshot 2021-10-27 213749.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1635350929799/bnTb0CZty.png)

![Screenshot 2021-10-27 214055.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1635351083473/vY7qeS-Dt.png)

❌**Don't do this**
![Screenshot 2021-10-27 214444.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1635351300986/61UUlutnr.png)

![Screenshot 2021-10-27 215344.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1635351839443/wPLy9K_fV.png)

## Making Pull Request
Your PR should do one thing. Always make a pull request for one part or section so that it would be easier for reviewers and maintainers to merge your pull request. If you are solving multiple issues in a project then open multiple PRs.

**Don't** make multiple PRs in one, this is confusing sometimes and also delayed the merging process. Let's assume you are making a PR for a new feature in the project and you also found a bug related to a different part of the same project. Don't fix that bug in the same PR. Because sometimes the other changes that gonna add value to the project get delayed due to multiple PRs in one. Make PRs small and on point, which will help your pull request getting merged easily.

**Don’t** open a PR like this:
- Fixes bug #343
- Adds new linting rules
- Includes feature #466

Attaching screenshots or some information related to your changes in the PR description is also very good practice. This will help the maintainer or reviewer to differentiate between changes.

✅**Do this**

![Screenshot 2021-10-27 233035.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1635357710905/HhuZ6VeLi.png)

❌**Don't do this**

![Screenshot 2021-10-27 233332.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1635357822392/sJpdNHose.png)

## Approvals and Dead PRs
**Don't** start working on any project before the maintainer gives you a go-ahead or assigned that issue to you. Don't open pull requests immediately. Wait for the maintainers approval 
- If the issue is already open and not assigned to anyone, ask maintainers if you can work on that.
- Start work on your PR.
- Don't ask maintainers to assign you an issue that is already assigned to someone else.

Sometimes you get confused during working on PR maybe you lost interest or whatever reasons please don't leave that open PR as it is, make sure to close that **dead PR**. The maintainer may not want to close it because they don't want to upset you. It neither looks good for the project nor to you. You can always reopen the Pull request if you want to work on that in the future.

## Be Meaningful
Every contribution is valuable. If something is broken in the project like an important link is not working in the documentation that will be needed to be fixed. But if you just change an emoji from ⚡ to 🚀, this is not much valuable. 

**Don't** break consistency. 
- Every time make sure to follow proper file order and directory to commit changes. 
- Removing semicolons, adding spaces, or making text bold in the project that doesn't prefer them.

## Hassling Maintainers To Merge
When you create any pull request or issue I know you get excited. Maintainers will get a notification that you raised or crested. You don't need to add additional comments and tag them. If it's taking time, give them a friendly call in comments that will be fine.

**Don't** hassle them on DMs on Twitter, Discord, Linkedin, or any other socials by sending them links of your issue or PRs. They are getting notifications from projects they maintain and you are adding more notifications. This will create more confusion for maintainers. Remember, most of these people maintaining projects are from different time zones. Many of them are maintaining open-source project in addition of their work. Be patience! You can give them a friendly reminder after 1 week or such.

✅**Do this**

![Screenshot 2021-10-28 004433.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1635362084267/UWbqUg1jJ.png)

❌**Don't do this**

![img.jpeg](https://cdn.hashnode.com/res/hashnode/image/upload/v1635362312519/6ML0tiARb.jpeg)

### References
[Eddie Jaoude](https://youtu.be/ExFCwFPTsE0)


#### If You ❤️ My Content! Connect Me on  [Twitter](https://mobile.twitter.com/Astrodevil_) or Supports Me By [Buying Me A Coffee☕](https://www.buymeacoffee.com/Astrodevil)







