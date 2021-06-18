---
title: Next steps for the books
summary: Thoughts on what needs to be completed and improved.
date: 2021-05-02
---

Time for a checkup on what I need to do/my thoughts on the two books.

I have taken a step back from completing the notes those last two months, because I felt overwhelmed by everything I had to do, life-wise. I need to finish the chapter on panel data analysis (and eventually the one on social network analysis), and I have to introduce the following chapters:

* Datamining: text analysis, web scrapping, mapping.
* Exploratory data analysis (_analyse géométrique des données_):
    * Correspondance analysis (_analyse factorielle des correspondances_),
    * Principal component analysis (_analyse en composantes principales_),
    * Multiple correspondance analysis (_analyse des correspondances multiples_),
    * Hierarchical clustering (_classification ascendantes hiérarchique_).
* (I am considering it) Quick introduction to RMarkdown.

I really like `bookdown`'s layout, but I am growing annoyed with having to knit the entire book whenever I add a new chapter or when I change the name of a single header. If I do not, the referencing goes haywire.

Which is why I am currently rebuilding the main book on `blogdown`, with Wowchemy's [project documentation template](https://github.com/wowchemy/starter-hugo-project-documentation) and with the deployment handled by Netlify. This workflow's advantage is that I can use `.md` files for simple text (Goldmark will then built the HTML files) and `.Rmardkdown` files for when I include some R codes. I knit those into Markdown files and that is it. No need to build the entire book every time.

I have not firmly settled on this method, I am only trying it out of curiosity.
