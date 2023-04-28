---
layout: single
title: "Technical instructions: contributing to the wiki"
tags:
  - manual
  - technical-doc
---

Here is some information material for anyone interested in contributing to the website (www.asellus.org), or the wiki-page (www.asellus.org/wiki). For the time being, we will use a git-workflow and pull-requests, which can be done quite conveniently via GitHub. For that you need a GitHub account, and some very basic git knowledge. People who possess both can skip to [pull requests](#pull-requests).

## TL;DR

If you just want to quickly add some content to the wiki and don't care about git:
1. make a [GitHub](https://github.com/) account and log in
2. go to the [source folder in the wiki repo on GitHub](https://github.com/The-Asellus-Consortium/asellus-wiki/tree/main/source)
3. edit a markdown file on GitHub (using the pencil symbol / obey [markdown syntax](https://kramdown.gettalong.org/quickref.html)) 
4. once done, click the "Propose changes" changes button (a consortium member that has access to [The Asellus Consortium](https://github.com/The-Asellus-Consortium) GitHub organization will see a "Commit changes" button instead)

## Basic info about git and GitHub

**Git** is a [version control system](https://en.wikipedia.org/wiki/Git) for tracking changes in files. It can be run on any OS (Window/Linux/Mac) and is widely used by programmers, scientists or anyone else who is working with code or text files inside a specified folder (=git repository). In a nutshell, git tracks changes in files, and allows you to trace back your progress in time. Moreover, it can compare changes between different versions of your files (they are called "branches"), and merge the changes made by different contributors:

<div style="text-align: center;width=500px">
  <img src="https://www.growingwiththeweb.com/images/2014/02/23/git-tree.svg"  />
	<figcaption>A git tree with different contributors (taken from <a href="https://www.growingwiththeweb.com/2014/02/a-gentle-introduction-to-git.html ">"A gentle introduction to Git"</a>).</figcaption>
</div>

**GitHub** is a company (owned by Microsoft) that offers webhosting of git repositories (for free). In a sense, GitHub is hardware, and git is software - so, a Git installation on your computer can communicate with the Github servers. There is some extra functionality of GitHub that is not directly offered by Git, such as the possibility to report code issues or have dicussions among contributors. GitHub also can generate websites directly from an online repository ([read this blog post](https://www.luerig.net/posts/website-with-gh-pages)) - however, the asellus community websites use [Netlify](https://www.netlify.com/products/build/) for this purpose.

## Setting up Git on your machine and clone the wiki

1. To install git on your local machine, follow these instructions: [Install Git](https://github.com/git-guides/install-git) (I recommend using the command line instead of GitHub Desktop). 

2. After installation, you first need to add a user name and email to the config file for git to know who is making changes to the tree. You can follow the [git tutorial](https://git-scm.com/docs/gittutorial) for these first steps. 

3. **For consortium members:** Once this is set up, you can log in to your account and clone the wiki repository from the consortium page: 

    `git clone https://github.com/The-Asellus-Consortium/asellus-wiki` 

	**For everyone else:** Once this is set up, you should log in to your account and "Fork" the wiki repository: [use the "Fork" button on the upper right](https://github.com/The-Asellus-Consortium/asellus-wiki). Now that you have made a copy to your account, you can "clone" (=download) a copy of the GitHub repo to your local machine using:

	`git clone https://github.com/MY-GITHUB-USERNAME/asellus-wiki` (replace `MY-GITHUB-USERNAME`)

## Make changes (and create a pull request)

{:start="4"}

4. Go to the cloned folder and you make changes to the documents in the source folder locally, with your favorite text editor. For formatting, follow the [markdown syntax](https://kramdown.gettalong.org/quickref.html). 

5. Once you have made some changes, you need to ["stage" and "commit"](https://git-scm.com/docs/gittutorial#_making_changes) them:

    `git add .` (`"."` will add all changed files to the tree index)<br>
  `git commit -m "added info on life history"`

6. Then you can push them back to the online repo you cloned from in the first place (for consortium members it is the original repo, for everyone else the forked repo):

    `git push`

7. **For consortium members:** you are done here!

    **For everyone else:**  Once the upload is completed, you need to go back to the repository on github, and create a [pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests), to signal consortium members that we should integrate the changes you made to the repo. For that, go to the tab "Pull requests" in the top row, and click on "New pull request". After that you should see all the changes you made in a "diff view". Create a message to be sent along with the pull request (e.g., describing what you changed), and click "Create pull request". 


## Further reading 

- [A gentle introduction to Git](https://www.growingwiththeweb.com/2014/02/a-gentle-introduction-to-git.html)
- [Authoring With Markdown
](https://carpentries-incubator.github.io/jekyll-pages-novice/markdown/)

