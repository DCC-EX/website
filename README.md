# DCC-EX Website Repository

This Repo holds all of the resources that together form the DCC-EX documentation website.

## Markdown

All pages on our site use github-flavored Markdown. For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

## Admonitions

Admonition is an extension included in the standard Markdown library that makes it possible to add block-styled side content to your documentation, e.g. summaries, notes, hints or warnings. See [Admonitions](https://squidfunk.github.io/mkdocs-material/extensions/admonition/) on squidfunk.

## Editing this repository

If you would like to contribute to this repository, please use Visual Studio Code or another text editor. Please do not use WYSIWYG editors for markdow such as typora - they destroy some of the finer formatting details like admonitions. We are always accepting pull requests - if you see a typo or something that needs clarification, we would love it if you would fix it for us!

## Pushing changes to the website

If you are a member of the DCC-EX organization, use the following steps to push changes from here to the live website. Clone the dcc-ex.github.io repository to the same folder as this repository on your computer. Once you've made your changes in this repo, navigate into the dcc-ex.github.io repository (NOT this one) and run the following command:
```bash
mkdocs gh-deploy --config-file ..\website\mkdocs.yml --remote-branch master
```
