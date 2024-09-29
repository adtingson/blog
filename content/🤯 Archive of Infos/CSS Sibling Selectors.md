---
title: How to Select Siblings in CSS?
draft: false
tags:
  - css
  - design
  - 🌿budding
date: 2024-09-30
---
I got so *used to styling individual elements and their children/decendants*, and I learned a lot of new tricks to style them. And while I was looking through the finished products of these stylings, I noticed something that bugged me off so much — *the lists* that follows the sentence or paragraph that introduced them *are not even sticking to the paragraph itself* 😠

So, I researched on conditional styling, because I needed to learn how to style if the selector should be “*if `<p>` is before `<ul>` or `<ol>`, then `p` should have `margin-bottom: 0`.*” And I was introduced to a new type of relative selectors in CSS — the **Sibling Selectors** 🥳

## What are They?

**The `+` Selector** — selects a sibling of an element.

```css
<div>
	<p>
		This is a paragraph. Here are some text.
	</p>
	<ul>
		<li>A list item.</li>
		<li>Another list item.</li>
	</ul>
	<ul>
		<li>A list item of this second list.</li>
		<li>Another list item.</li>
	</ul>
</div>

<style>
	p + ul {
		color: red;
	}
</style>
```

So, that example above basically says that *select the first `ul` element* because it is a *sibling of `p`* and color the text red. So, the first list will be red, *but the second one won’t be*.

**The `~` Selector** — selects *all the sibling elements* of an element.

```css
<style>
	p ~ ul {
		color: red;
	}
</style>
```

Same as the `+` above, but this time *both `ul`* will be colored red because *they are all siblings of `p`*.

## What if I Want to Select a Previous Sibling?

This became *my new problem* because *there is no selector* for that! 🥲 I want to select the `p` and not the `ul`, but luckily there is a pseudo-selector called `:has()`.

```css
<style>
	p:has(+ ul) {
		color: red;
	}
</style>
```

So, basically what the code says is that select `p` **that has** a sibling `ul`. And if that was run for the example above, *the paragraph* will be colored red *instead of the lists* 🥳🎉