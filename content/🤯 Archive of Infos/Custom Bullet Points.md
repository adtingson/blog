---
title: Custom Bullet Points
draft: false
tags:
  - "#design"
  - css
  - improvements
  - development
  - web-design
  - 🌿budding
date: 2024-09-19
---
- Make `<li>` markers *invisible* and replace it *with a custom marker*
	- Got this idea from Minimal theme in Obsidian
- 👍 Can create custom bullets using emojis or SVGs
- 👍 Can make correct postioning for bullets *for aesthetics*
- 👍 New opportunity to learn more CSS
- I can impliment this the same way Obsidian renders custom checkboxes
	- I need to study this shit 😭
- I can try to modify Quartz’s *Obsidian Flavored Markdown Plug-in* to add the `data-task` property to list items

## Progress So Far…

- [x] **Test** how Quartz render *normal Markdown* lists and checkboxes vs my *Obsidian custom* checkboxes
- [ ] Tinker with Quartz’s *Obsidian Flavored Markdown Plug-in* to add `data-task`
- [ ] Impliment it to my Digital Garden

## Snippets

### Testing List Items via This Markdown

```
- normal list
- [ ] normal checkbox
- [p] obsidian custom checkbox: "pro/thumbs up"
```

- **Obsidian Render**
	- ![[custom bullet obsidian render.png]]
- **Quartz Default Render**
	- ![[custom bullet quartz default.png]]