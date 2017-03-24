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
When more than one selector shares the same declaration, they may be grouped together via a comma-separated list. This allows you to reduce the size of the CSS (every bit and byte is important) and makes it more readable. The following snippet applies the same background to the first three heading elements.

    h1, h2, h3 {background: red;}

**2. What is the difference between an ID selector and a CLASS?**

An ID selector identifies and sets style to only one occurrence of an element, while CLASS can be attached to any number of elements.

## **2a.  How does the hierarchy of selectors work**![selectorhierarchy.png](/uploads/selectorhierarchy.png)

  The picture sums it up here,  Element > Class > ID.  The more specific your selector is the more it will override.

## **3. Inline vs Inline Block vs Block(default)**

*  Inline  elements  can have other elements sit next to it on left and right but keep there margins and padding on the left and right. Inline elements however do not respect top and bottom margins/padding therefore they cannot have a height set, nor can it have a width set.


*  Block elements  respect all margins and padding's, it also forces a line break after the element. Display: Block is the default value.

* Inline-Block element's do all that inline does, but additionally it can have a height and width, as well as respects all the margins and padding.

  ![inlinevsinlineblock.png](/uploads/inlinevsinlineblock.png)

4\.