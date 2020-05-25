# Convert Markdown to PDF: Pandoc Links and Hyperlinks

Keywords: convert, markdown, pdf, hyperlink, blue, cyan, link, color

## Motivation

Currently, [Pandoc](https://pandoc.org/getting-started.html) has been the most
reliable way to convert markdown files (`.md`) to `.pdf` files. Unfortunately,
the default converting process does *not* highlight links with blue (instead,
they are colored the default text color black, although clickable). Knowing 
how to do this apparently required reading the instruction manual. Luckily, 
someone pointed out the section I should read in [this thread](https://groups.google.com/forum/?utm_medium=email&utm_source=footer#!msg/pandoc-discuss/EhXTHbvEv-w/nHYzWtCTAgAJ).
I was a fool for thinking that people didn't think of this, but maybe they're the fools for not enabling this feature by default.

This short document will show you how to convert markdown to PDF *with* colored links and hyperlinks.

Example: [This document rendered using the command below]() (In progress... TODO).

## How to Convert Markdown to PDF *with* Colored Links

So let's say you have a markdown file called `notes.md` and you want to convert
it to `notes.pdf`. You also want to:

- Highlight all hyperlinks in `cyan`
- Highlight all internal links in `cyan`

Yes, apparently there is a difference between the two (unlike how it's rendered
in GitHub-flavored markdown). Here's the command for that:

```bash
$ pandoc notes.md -o notes.pdf -V linkcolor=cyan -V urlcolor=cyan
```

You can replace `cyan` with whatever color you want, as long as it is allowed by
[`xcolors`](https://en.wikibooks.org/wiki/LaTeX/Colors#Predefined_colors) in LaTeX.
