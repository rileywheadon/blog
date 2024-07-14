---
layout: default
title: How I Take Notes
draft: true
---

# How I Take Notes

I'm convinced that ***so much good information goes to waste***.

Every day I get bombarded with more information than I could possibly remember. From lectures to videos to random blog posts that I stumble across in my spare time, I'd have to estimate that my brain *truly* remembers maybe 10% of what I consume. Before I started using a knowledge management system, the other 90% of stuff would come back to haunt me. "I'm pretty sure I learned how to do XYZ before, but I forgot and now I have to Google it again" was a common experience while doing just about anything. And this *really* bothered me, because I hate doing things twice. To fix this problem, I started taking a *lot* of notes. This got messy fast, so I started developing a system to keep organized. After a years worth of effort, my system has grown to hundreds of notes and drastically improved my productivity.

In this post, I'm going to outline exactly *how* and *why* I take notes. Of course, what I do is tailored to my personal needs, and certainly won't work for everyone. At the very least, I hope that reading this leaves you with some interesting ideas for developing your own knowledge management system.

## Obsidian

All of my note taking is done digitally in [Obsidian](https://obsidian.md/). I'm not going to explain how Obsidian works (there's an excellent tutorial [here](https://help.obsidian.md/Home)), but I will outline why I use it. First of all, Obsidian has an extremely low barrier to entry while also being enormously customizable and extensible. The plugin ecosystem for Obsidian is unmatched, I swear it has solutions for every conceivable use case and more. Another advantage of Obsidian is that notes are stored as [Markdown](https://en.wikipedia.org/wiki/Markdown) files, so your notes will remain accessible even if Obsidian were to be discontinued. Since notes are stored locally, Obsidian gives you complete autonomy over your data, unlike cloud-based software such as [Notion](https://www.notion.so/) and Google Drive. Finally, Obsidian lets me edit my notes using [vim-like](https://publish.obsidian.md/hub/04+-+Guides%2C+Workflows%2C+%26+Courses/for+Vim+users) key bindings, which makes editing text *so* much faster. Everyone who spends a lot of time on their computer should learn vim, its legitimately life changing.

# Additional Content

You can view my previous posts on Obsidian here:

- <a href="why-obsidian.html">Why Obsidian?</a>
- <a href="fast-typesetting.html">Fast Typesetting with Obsidian Plugins</a>

This post is meant to provide a general overview of how I use Obsidian to take notes in my university classes.

## The Fuzzy Finder

The **Fuzzy Finder** is Obsidian's mechanism for searching your vault. You can open it by pressing `CMD + O`, which should bring up a window like this:

<div style="text-align: center"><img width="600" src="/assets/images/fuzzy-finder.png"></div>

(If you're wondering, the folder numbers are <a href="https://johnnydecimal.com">Johnny Decimal</a>)

When I type in the search bar, Obsidian will locate notes by folder and title *simultaneously*. Then, by pressing `CMD + ENTER`, I can open the top search result in a new tab.

Why is a search bar like this so useful?

The fuzzy finder is built into Obsidian, which means I can create, delete, and switch between notes without having to open a file explorer. This means that I can easily edit multiple notes at the same time.

Because the fuzzy finder displays the file path, it's possible to differentiate notes by both their title *and* their location. Consider the following file tree:

```
/MATH-100
	formula-sheet
/PHYS-131
	formula-sheet
```

If I search for `MATH 100 formula sheet`, the fuzzy finder will only display the file in the MATH 100 folder, which allows me to have many notes with the same title across my vault.

## One Idea, One Note

Because the fuzzy finder allows me to search my entire vault, I want my file paths and note titles to be as intuitive as possible. The rule I use for this is *one idea, one note*.

In practice, this is how this apply this principle:

- Do not create separate notes for examples. Instead, include them under a `## Examples` header in the note for the concept it is demonstrating.
- A note should not contain more than one formula.
- A note should not explain pre-requisite concepts. Instead, provide a link to another note.
- Notes should be as long as needed to explain the concept, but no longer.

## Creating a Class

Every class has the following folders:

- `Notes`, which contains exclusively markdown notes. This folder has a file with the star emoji (⭐️) which contains the class time, class location, and links to other notes.
- `Figures`, which has any pictures that I use in my notes.
- `Resources`, which contains any information related to the course like class slides, class notes, or the textbook.

# Useful Plugins

## Obsidian LaTeX Suite

The <a href="https://github.com/artisticat1/obsidian-latex-suite">Obsidian LaTeX Suite</a> allows me to easily type <a href="latex-guide.html">LaTeX</a> using a set of customisable snippets. I wrote a separate guide on using the plugin, which can be found <a href="fast-typesetting.html">here</a>.

## Filename Heading Sync

This plugin automatically changes the name of the file to the first heading, and vice versa. I recommend this plugin because it forces you to implement the one idea, one note rule.

## Advanced Tables

Markdown tables are pretty awful to use by default. This plugin provides some excel-like functionality such as:

- Using `TAB` to cycle through cells
- Hotkeys to add and remove rows / columns
- Automatic alignment of table border characters
