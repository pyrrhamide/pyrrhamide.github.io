---
title: Customising a bookdown project
summary: CSS on bookdown and a word on `blogdown`/Netlify/Hugo.
date: 2021-05-29
---

Here is a list of the major changes on my `bookdown` project, specifically changes to the regression book. I'm keeping the other one as it is, for comparison's sake:

* Fonts: main text - Lato (now Mulish because I change fonts like I change underwear); headers - Zilla Slab. Quick note for future endeavours: always import the bold version of your font, otherwise the renderer will do it itself and it might look dodgy.
* Links colour (active links, main text, hover) in blue...aquamarine?
* Active link + h1 headers (except title) styled in blue + border left,
* Title: larger font.
* Added a favicon.

I have also added the skeletons files for the remaining chapters I had planned, and finalised the RMarkdown chapter.

Issue with `blogdown`/Netlify/Hugo:

* MathJax equations are not showing when browsing. Instead, the Markdown syntax is visible. You have to refresh the page to get stuff to work.

This is an unfortunate drawback that makes me believe I will not pursue this new workflow.