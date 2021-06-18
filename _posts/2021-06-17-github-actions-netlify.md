---
title: Deploying bookdown on Netlify, using Github Actions
summary: Changing my workflow, not building the whole book anymore, winning at life.
date: 2021-06-17
---

As I previously expressed, I grew annoyed at having to build the book every time I was changing something minor (or major but that is more understandable). I tried using Wowchemy's project template to rewrite everything, but there were issues with equation-rendering.

I then fell upon [Emil Hvitfeldt "Deploy your bookdown project to Netlify with GitHub Actions"](https://www.hvitfeldt.me/blog/bookdown-netlify-github-actions/) post, which did not need Jekyll: I tried it out with the `bookdown` [demonstration book](https://github.com/rstudio/bookdown-demo), then with my own and [it worked out](https://tiramisurules.netlify.app) quite nicely.

I have some points to raise about the whole process:

* I properly identified myself for the `usethis` package (in particular, regarding the Personal Access Token thingy),
* I added a DESCRIPTION file: `usethis::use_description(check_name = FALSE)`,
* I removed the output folder `docs` (necessary for GitHub pages) in the `_bookdown.yaml` file,
* In the `bookdown` demonstration book, we can find `.travis.yml`, `Dockerfile`, `_build.sh` and `_deploy.sh`. These files are not needed here.
* `renv::snapschot()` is chatty: read it all. I forgot to type `y` because it looked like it was finished, but it was not.
* It is very slow. It took [12 minutes](https://github.com/pyrrhamide/qessreg-netlify/runs/2847510272) to build and deploy.

All in all though, it is less trouble for me and less space taken on my hard drive. I might add a `_redirects` file at some point, to redirect traffic from GitHub pages to Netlify. This was more of an exploration of GitHub Actions and of `usethis` if anything.