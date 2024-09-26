---
title: Better Bullet Point Positioning 🎯
draft: false
tags:
  - css
  - design
  - improvements
  - 🌿budding
date: 2024-09-26
---
## The Problem

![[Better Bullet Positioning 1.png]]

As you can see, the **bulleted point** is *rendered on the bottom-left* of the image in the list item. I need to make it *rendered on the top-left*.

## Solution

- [x] Make the *default bullet invisible*

```css
article.popover-hint ul li {
    list-style-type: none;
}
```

- [x] *Replace default bullet* with a similar-looking bullet (`\2022`) and position it in the *correct spot*
	- We need to replace it because the *default one can’t be styled for positioning*

```css
article.popover-hint ul li::before {
    content: "\2022 "; // bullet point code
    color: var(--darkgray); // coloring
    font-size: 1.5rem; // sizing
}
```

- [ ] ~~Use *CSS Flexbox* for this~~
	- **Flexbox is a fail** because I forgot that *for it to work* you will need the `<li>` to be styled as `display: flex;` but these elements need to be `display: list-item` *for them to display as lists* 😅
- [x] Use *old-school CSS* styling instead 💪

```css
article.popover-hint ul li::before {
    margin-left: -1rem; // move the bullet one font-size to the left
    float: left; // make the bullet float to the leftest left (the upper-left)
}
```

## ⚠️ Result

![[Better Bullet Positioning 2.png]]

- 🎉 **Major Success**!! 😁