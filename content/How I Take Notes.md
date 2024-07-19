---
layout: default
title: How I Take Notes
draft: true
---

# How I Take Notes

I'm convinced that ***so much good information goes to waste***.

Every day I get bombarded with more information than I could possibly remember. From lectures to videos to random blog posts that I stumble across in my spare time, I'd have to estimate that I *truly* remember maybe 10% of what I consume. Before I started using a knowledge management system, the other 90% of stuff would come back to haunt me. "I'm pretty sure I learned how to do XYZ before, but I forgot and now I have to Google it again" was a common experience while doing just about anything. And this *really* bothered me, because I hate doing things twice. To fix this problem, I started taking a *lot* of notes. This got messy fast, so I began developing a system to keep organized. After a years worth of effort, my system has grown to hundreds of notes and drastically improved my productivity.

In this post, I'm going to outline exactly *how* and *why* I take notes. Of course, what I do is tailored to my interests and needs, and it certainly won't work for everyone. At the very least, I hope that reading this leaves you with ideas and motivation for developing your own knowledge management system.

## Philosophy

As I mentioned in the introduction, my goal is to *never* have to relearn a piece of information. What this means is that every time I learn a new mathematical theorem of piece of software, I'll create a brief note and write down any important details. The information that goes into my system comes from a variety of sources, including lectures, books, blogs, podcasts, and videos. Now you might be thinking that taking notes on a blog is overkill, but hear me out. Taking notes forces you to not just understand the media you're consuming, but summarize it.

![[blooms.jpeg]]

On Bloom's taxonomy ([source](https://www.valamis.com/hub/blooms-taxonomy)), taking notes moves you from remember/understand to at least apply. If you're being thorough, note taking helps you to deeply analyze what your reading and find connections with other ideas. Yes, taking notes on a piece of media probably takes 2-3x longer than just reading it. But this is a tradeoff I'm willing to make. I'd rather read one book, learn it well, and have a list of ideas to come back to later than read three books haphazardly in the same time. If I learn something I think is useful, I'll write it down. Simple as that.

When actually taking notes, I live by the rule *one idea, one note* principle. In practice, this is what that means:

- With some exceptions, I don't make a note for each piece of media I consume. Instead, I add ideas from what I'm currently reading to related notes I already have.
- Note length isn't important to me. Some ideas require a lot of justification or context, while others can be as short as 2-3 sentences.
- I do not create separate notes for examples or practice problems. Instead, include them under an `Examples` or `Exercises` header within an existing note.
- I do not explain pre-requisite concepts in my notes. Instead, I provide a link to another note which does.
- I believe that if a note really represents one idea, its title should be short. When I'm unable to think of a concise title for a note, it probably means the note shouldn't exist.

## Obsidian

All of my note taking is done digitally in [Obsidian](https://obsidian.md/). I'm not going to explain how Obsidian works (there's an excellent tutorial [here](https://help.obsidian.md/Home)), but I will outline why I use it. First of all, Obsidian has an extremely low barrier to entry while also being enormously customizable and extensible. The plugin ecosystem for Obsidian is unmatched, it ought to have solutions for every conceivable use case and more. Another advantage of Obsidian is that notes are stored as [Markdown](https://en.wikipedia.org/wiki/Markdown) files, so your notes will remain accessible even if Obsidian were to be discontinued. Since notes are stored locally, Obsidian gives you complete autonomy over your data, unlike cloud-based software such as [Notion](https://www.notion.so/) and Google Drive. Finally, Obsidian lets me edit my notes using [vim-like](https://publish.obsidian.md/hub/04+-+Guides%2C+Workflows%2C+%26+Courses/for+Vim+users) key bindings, which makes editing text *so* much faster. Everyone who spends a lot of time on their computer should learn vim, its legitimately life changing.

## File Structure

The layout of my Obsidian vault is roughly based on the [Johnny Decimal](https://johnnydecimal.com/) system. I like this philosophy for arranging my folders because it places a hard limit on the amount of depth in my file tree. Why is depth bad? When you create a new file in Obsidian, it gets placed in the same folder as the file you currently have open (you can also change your settings to put new files in a set folder, but this is even worse). Thus to avoid moving files around manually, it makes sense to keep your file tree as shallow as possible. Additionally, the breadth of your file tree is no issue, since Obsidian allows me to search my entire vault at once. You *could* put every single note and image into the root of your vault and Obsidian would work just fine. The issues start when you need to get all the files related to a certain topic. Then, [tags](https://help.obsidian.md/Editing+and+formatting/Tags) or folders are a godsend. Essentially, if you're using Obsidian I would recommend trying to use as few folders as possible while still maintaining some semblance of structure.

Since my entire vault contains hundreds of notes, it can help to create notes whose sole purpose is to link to other notes. I like to prefix these notes with the star ⭐️ emoji, which conveniently moves them to the top of the file explorer in the sidebar. If I have multiple layers of indexing notes, I'll prefix the second layer with the house 🏠 emoji, which will move these notes to just beneath the starred notes in the file explorer.

Just to provide a general example of what my file structure looks like in practice, here's a snapshot of my "University" folder:

```
/30 University
	/31 UBC
		Schedule.md
		Course Planning.md
		Todo.md
	/32 MATH 320
		/32.01 Notes
			⭐️ MATH 320.md
			...
		/32.02 Resources
			math-320-textbook.pdf
		/32.03 Assignment 1
			main.tex
			...
			main.pdf
	/33 MATH 322
	...
```

## The Fuzzy Finder

The **Fuzzy Finder** (`CMD + O`) is Obsidian's mechanism for searching your vault. When I type in the search bar, Obsidian will locate notes by folder and title *simultaneously*. Then, by pressing `CMD + ENTER`, I can open the top search result in a new tab.

This is extremely useful because it allows me to create, delete, and switch between notes without having to open a file explorer. Because the fuzzy finder displays the file path, it's possible to differentiate notes by both their title *and* their location. Consider the following file tree:

```
/MATH-100
	formula-sheet
/PHYS-131
	formula-sheet
```

If I search for `MATH 100 formula sheet`, the fuzzy finder will only display the file in the MATH 100 folder, which allows me to have many notes with the same title across my vault.

## Plugins and Extensions

### LaTeX Suite

The [Obsidian LaTeX Suite](https://github.com/artisticat1/obsidian-latex-suite) allows me to rapidly typeset $\LaTeX$ using a set of customizable snippets. I'm not going to expand on this plugin too much, since I already wrote a separate guide on it [[Fast Typesetting with Obsidian LaTeX Suite|here]].

### Advanced Tables

Obsidian allows you to edit text in two ways--live preview and source mode. Since I type a lot of $\LaTeX$ in my notes, I prefer use source mode in order to see the exact characters I'm typing. Unfortunately, this means I can't use the new [Table Editor ](https://obsidian.md/changelog/2023-12-26-desktop-v1.5.3/), which only works in live preview mode. To get around this problem, I use the [Advanced Tables](https://github.com/tgrosinger/advanced-tables-obsidian) plugin, which gives me the functionality I need in source mode. Particularly, I am able to:

- Use `TAB` to cycle through cells
- Bind hotkeys to insert and delete both rows and columns
- Automatically align table border characters
- Add basic excel-like formulas to my tables

This plugin only works in source mode, so if you use live preview, I would just stick to the built-in table editor.

### Citations

I've doing research since the may, and this means dealing with *a lot* of sources. I began using [Zotero](https://www.zotero.org/) to keep track of my references, but I wanted to have access to them within my Obsidian vault. The way I added this functionality was with the [Citations](https://github.com/hans/obsidian-citation-plugin) plugin, which automatically imports sources from a Zotero folder. Note that the [Better BibTeX](https://retorque.re/zotero-better-bibtex/) Zotero extension is necessary for this to work. The citations plugin also allows me to create "literature notes" from any source, which automatically import the source's metadata.

### Excalidraw

I do not own a drawing tablet, so its nice to have a way to create quick, informal diagrams. I've found the [Excalidraw](https://github.com/zsviczian/obsidian-excalidraw-plugin) plugin to work great for this use case. My favourite feature from this plugin is the ability to seamlessly import drawings into my notes without having to worry about exporting images from another piece of software.

### Linter

The [Obsidian Linter](https://github.com/platers/obsidian-linter) plugin ensures that the markdown files within your vault are formatted consistently. It can do things like add a line break above and below lists, automatically capitalize headings, and remove consecutive empty lines. This normally wouldn't matter to me but Pandoc (see below) can get really picky about markdown syntax.

### Pandoc

[Pandoc](https://pandoc.org/) has grown to be an *extremely* important part of my workflow. It is not an Obsidian plugin, but rather a CLI application that allows me to export markdown files to almost any other file type. What this allows me to do is typeset $\LaTeX$ documents in the much simpler markdown syntax, and then export them to a PDF using Pandoc. I've used this to write research reports, do assignments, and create presentations using [Beamer](https://www.overleaf.com/learn/latex/Beamer). If you're someone who finds formatting documents in $\LaTeX$ to be overly tedious, I would *highly* recommend giving Pandoc a try.

Of course, Pandoc trades control over document formatting for writing speed. For me, this is a sacrifice I'm willing to make. However, if you need to create professional documents or typeset research articles, it might be better to stick with $\LaTeX$.

### Quartz

[Quartz](https://quartz.jzhao.xyz/) is the incredible piece of software I use to turn my Obsidian vault into a "mini-blog". It seamlessly converts Obsidian-style markdown files to webpages, and does so in a way that makes it easy to add links and attachments. Obviously, my website doesn't have all the features of a real blog, like comments and feeds. But I can quickly push new "posts" and easily control the layout and style of my website, which is all I need for now. If you're interested in publishing your writing quickly and easily, I would recommend giving Quartz a try. Its even more straightforward than other lightweight blogging software like [Jekyll](https://jekyllrb.com/).

## Conclusion

My Obsidian vault has grown to be more than just a note-taking system. I now use it to make to-do lists, make schedules, journal, and of course, take notes. Using plugins and external software, I've extended my Obsidian vault to the point where it is the only software I need to produce documents of all kinds. By developing an efficient system for note-taking, I've made it easier to process the enormous amount of information I'm exposed to every day. This has helped me learn faster, write better, and study easier. If you're interested in trying something similar, the best time to start is now. *Just start writing*.
