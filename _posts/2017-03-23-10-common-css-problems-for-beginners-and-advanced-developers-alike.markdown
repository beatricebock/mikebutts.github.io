---
title: 10 Common CSS problems for beginners and advanced developers alike
date: 2017-03-23 16:11:00 -05:00
categories:
- tutorials
tags:
- tutorial
- beginner
- CSS
main_img: https://pace.oregonstate.edu/sites/default/files/styles/course_banner_large/public/images/course/cover/pace-oregon-state-html-css-coding-web-design.jpg?itok=tNEZncCn
layout: post
---

![Q3cUg29.gif](/uploads/Q3cUg29.gif)

CSS can be frustrating when working on a project,  you type in XYZ and the result looks like ABC and you have no idea why. So I thought up some of the most common mistakes or misconceptions you might run into. Let's hop into:

### **1. What is Grouping?**

When more than one selector shares the same declaration, they may be grouped together via a comma-separated list. This allows you to reduce the size of the CSS (every bit and byte is important) and makes it more readable. The following snippet applies the same background to the first three heading elements.

    h1, h2, h3 {background: red;}

### **2. What is the difference between an ID selector and a CLASS?**

An ID selector identifies and sets style to only one occurrence of an element, while CLASS can be attached to any number of elements.

### **2a.  How does the hierarchy of selectors work**

![selectorhierarchy.png](/uploads/selectorhierarchy.png)

The picture sums it up here,  Element > Class > ID.  The more specific your selector is the more it will override.

### **3. Inline vs Inline Block vs Block(default)**

* Inline  elements  can have other elements sit next to it on left and right but keep there margins and padding on the left and right. Inline elements however do not respect top and bottom margins/padding therefore they cannot have a height set, nor can it have a width set.


* Block elements  respect all margins and padding's, it also forces a line break after the element. Display: Block is the default value.

* Inline-Block element's do all that inline does, but additionally it can have a height and width, as well as respects all the margins and padding.

  ![inlinevsinlineblock.png](/uploads/inlinevsinlineblock.png)

### **4. White-space does not matter.**

For the record, it does not matter if you have spaces or do not, however, I would not hire you if it was hard to read!
\[!\[whitespace\](/uploads/whitespace.jpg)\](/uploads/whitespace.jpg)

### **5. Pseduo Class, what are they?**

Pseduo classes allow you to identify HTML elements based on characteristics
!\[pseduo class\](/uploads/psuedo.png)

### **6. Child class vs multiple classes**

When you have .bob .sue (with a space), this means sue is a child of bob. When there is no space, .bob.sue the class declaration in the div have to have both bob and sue in it.
!\[child class vs multiple classes\](/uploads/childvsmultiple.png)

### **7. Why does my CSS have weird margins?**

CSS by default have margins and padding that might be affecting your code. To fix this you can make a reset.css file and paste the following:\*\*

    html, body, div, span, applet, object, iframe,
    h1, h2, h3, h4, h5, h6, p, blockquote, pre,
    a, abbr, acronym, address, big, cite, code,
    del, dfn, em, img, ins, kbd, q, s, samp,
    small, strike, strong, sub, sup, tt, var,
    b, u, i, center,
    dl, dt, dd, ol, ul, li,
    fieldset, form, label, legend,
    table, caption, tbody, tfoot, thead, tr, th, td,
    article, aside, canvas, details, embed, 
    figure, figcaption, footer, header, hgroup, 
    menu, nav, output, ruby, section, summary,
    time, mark, audio, video {
        margin: 0;
        padding: 0;
        border: 0;
        font-size: 100%;
        font: inherit;
        vertical-align: baseline;
    }
    /\* HTML5 display-role reset for older browsers \*/
    article, aside, details, figcaption, figure, 
    footer, header, hgroup, menu, nav, section {
        display: block;
    }
    body {
        line-height: 1;
    }
    ol, ul {
        list-style: none;
    }
    blockquote, q {
        quotes: none;
    }
    blockquote:before, blockquote:after,
    q:before, q:after {
        content: '';
        content: none;
    }
    table {
        border-collapse: collapse;
        border-spacing: 0;
    }

### **8. Use DRY code (Don't Repeat Yourself)**

Reusing code is a common problem with beginners, often I will see someone have multiple classes all using similar css for example

font-weight: bold;
color: #0000FF;
border-top: 1px solid blue;

Instead having the repeat code in multiple classes, you could make it, it's own class and have div class="oldclass newclass". Another DRY mistake is not using short hands. .one, .two, .three and .four in the image all accomplish the same thing.

### **9. CSS on Elements**

Don't use css on elements unless you have a good reason (p{color: red}), use classes!

### **10. Relative vs Absolute**

http://stackoverflow.com/a/20718728
And
https://blog.kevinchisholm.com/css/absolute-positioning-basics/