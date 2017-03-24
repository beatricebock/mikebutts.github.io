---
title: 10 Common CSS problems for beginners and advanced developers alike
date: 2017-03-23 16:11:00 -05:00
categories:
- tutorials
tags:
- tutorial
- beginner
- CSS
---

![Q3cUg29.gif](/uploads/Q3cUg29.gif)

CSS can be frustrating when working on a project,  you type in XYZ and the result looks like ABC and you have no idea why. So I thought up some of the most common mistakes or misconceptions you might run into. Let's hop into:

**1. What is Grouping?**

     When more than one selector shares the same declaration, they may be grouped together via a comma-separated list.       This allows you to reduce the size of the CSS (every bit and byte is important) and makes it more readable. The following snippet applies the same background to the first three heading elements.

h1, h2, h3 {background: red;}

**2 What is the difference between an ID selector and a CLASS?**

An ID selector identifies and sets style to only one occurrence of an element, while CLASS can be attached to any number of elements.
