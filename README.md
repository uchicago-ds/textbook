# The UChicago Data 8 Jekyll textbook

This repository holds UChicago's fork of the Data 8 Berkeley textbook.

To date, there are no content changes, only changes to [_config.yml](_config.yml) to point to UChicago's Jupyterhub and to define the correct host. No deployment steps are needed as it is handled by Github Pages. 

Everything below this line is from the original data8 textbook README.

-------

All textbook content is primarily stored in Jupyter notebooks in the `content/` folder.
This can be converted to Jekyll-ready markdown and served on github pages.

## How this repository is deployed to `inferentialthinking.com`

The Data 8 textbook has a slightly more complex deploy process. This is because
[GitHub doesn't work well for using a custom domain name for an organization's non-root
repository](https://help.github.com/articles/custom-domain-redirects-for-github-pages-sites/).

So, here's how the textbook deploy works:

* The textbook at `inferentialthinking.com` is actually being served from this repository:

  https://github.com/inferentialthinking/inferentialthinking.github.io

  **You should not ever directly edit the inferentialthinking.github.io repository**
* Updates to the textbook should be made at **this** repository (`github.com/data-8/texbook`)
* When you make a change to this repository and push it to the `data-8/textbook` gh-pages
  branch, these changes should automatically be copied to https://github.com/inferentialthinking/inferentialthinking.github.io.
* This is done with CircleCI, and the [configuration for this can be found](.circleci/config.yml)

## Building the textbook
Here are steps to get started building the textbook on your own machine:

1. **Install the jupyter-book command line tool**. This allows you to create
   and modify Jupyter Books:

   ```
   pip install jupyter-book
   ```

2. **Follow the build instructions on the Jupyter Book guide**. The guide
   has information for how to use the Jupyter Book CLI to build this book.
   You can find the [Jupyter Book build instructions here](https://jupyter.org/jupyter-book/guide/03_build.html#build-the-books-markdown).

**To preview your built site** using Jekyll on your computer, follow
the steps on the [Jupyter Book guide](https://jupyter.org/jupyter-book/guide/03_build.html#build-the-books-site-html-locally-optional).

## Relevant files

An explanation of the various files in this textbook can be found in
the [Jupyter Book guide](https://jupyter.org/jupyter-book/guide/01_overview.html#a-quick-tour-of-a-jupyter-book).
