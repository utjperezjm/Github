#How to get started with GitHub
Compiled by Ashley Shade for EDAMAME2016. Contributors: John Chodkowski and Jackson Sorenson
[EDAMAME-2016 wiki](https://github.com/edamame-course/2016-tutorials/wiki)

***
EDAMAME tutorials have a CC-BY [license](https://github.com/edamame-course/2015-tutorials/blob/master/LICENSE.md). _Share, adapt, and attribute please!_
***

##Overarching Goal
* This tutorial will contribute towards building **computing literacy**, specifically towards computing workflow development and version control.

##Learning Objectives
* Set up a GitHub Account
* Initialize a GitHub Account using the command line
* Pull a repository
* Basic git commands:  `pull`, `push`, `status`, `add`, `commit`
* Markdown syntax for text-to-html conversion

***
_Preamble_:  GitHub provides excellent resources, and most of this tutorial points to existing GitHub documentation.   

##1.  Create a GitHub [account](https://github.com).

##2.  Set up Git on your [personal computer](https://help.github.com/articles/set-up-git/)
*  Download git by clicking on the link
*  Configure git using `git config`.  Note there are separate instructions for Mac, Windows, and Linux users.
*  Authenticate with GitHub.  We suggest using [HTTPS for cloning](https://help.github.com/articles/which-remote-url-should-i-use/#cloning-with-https-recommended), and [cache-ing](https://help.github.com/articles/caching-your-github-password-in-git/) your GitHub password. Note there are separate instructions for Mac, Windows, and Linux users.
*  If you're a Windows user, you'll also have to download Gitbash in order to use git commands. Download this [here](https://git-for-windows.github.io).


##3.  Fork and Clone a repository
The main benefit of forking a repository is that it allows you to copy an existing repository and then have the ability to make your own edits to the repository without changing the original repository.
*  Navigate to the EDAMAME [2016-tutorials](https://github.com/edamame-course/2016-tutorials) repository.  
*  On the upper right-hand side there is a box labeled "Fork". Click on that.

![img1](/img/Fork.png)

*  You'll be re-directed to your github account. The repository is now on your github account but we still need to clone the repository so we have local access to the files.
*  In the new window, on the right hand side there is a box labeled "Clone or download".

![img2](/img/Clone.png)

* Click on that and then copy the link by clicking on the clipboard icon.
*  Choose a local directory that you want this repository to be added to. Change into that directory and clone the URL just copied:

```
git clone https://github.com/edamame-course/2016-tutorials.git
```

*  Directions for 'git clone' can also be found at [GitHub](https://help.github.com/articles/cloning-a-repository/).
*  This protocol can be used to clone any public repository.  For EDAMAME repos, you can `pull` to get the most up-to-date materials from GitHub, but you cannot `push` to edit those resources and have your edits tracked to the main repository, because you are not part of the EDAMAME team. (More details on these commands below).

##4.  Basic git commands
*  There is are a few youtube video tutorials that are a good introduction to git and version control.  Here is [one](https://www.youtube.com/watch?v=0fKg7e37bQE).  We recommend that you work through the video with the instructor, pausing and starting again as needed, to get started with Git.
* All git commands start with `git`.  Git commands will only work within git repositories (you can't use them on any old directory on your computer).

* The sequence of adding new files / updating a repo.
  - There is a sequence that is used to add something new to a github repo: git status, git pull, git add, git commit, and git push. The first two commands are extremely important if you're working in a shared repository with other collaborators. Since all collaborators may be making edits to the same document, you want to make sure you have the most up-to-date file before you make edits and submit your edits on a file to the repository. First, you use `git status` to determine if your files on your computer are different from the files on the remote git repository.  If it is different, use `git pull` to make sure you are working with the most recent files, which will prevent conflicting edits with your team mates.

 - For more information on [git status](https://git-scm.com/docs/git-status) and [git pull](https://git-scm.com/docs/git-pull), see here and here. However, since we forked an EDAMAME repository, you currently have no collaborators. Since you are the sole editor of these files, git status and git pull are not needed.

* Now, let's make a local edit and submit it to your github repository.

* Change into the tutorial directory that we forked and cloned before. **Remember, Windows users should be using gitbash for all of these steps!**

```
cd \path\to\directory\of\forked\repository
```

* Using your favorite text editor, let's open the README.md file. nano for Mac and Linux and notepad for Windows are default options, but you can find info for more advanced? text editors such as atom (MAC and Linux) and sublime (Windows) below.

Mac and Linux users
```
nano README.md
```

Windows users

```
notepad.exe README.md
```

Make any edit you want to the document, save it, and then close.

We have made edits on our local computers, but these edits have not been uploaded to our github repository. We will use git add, git commit, and git push to do so.

* Use `git add` to start tracking changes to an existing file.  
```
git add FILENAME
```

In our case,
```
git add README.md
```

* Use `git commit` to create a git version control. A brief message after the `-m` flag must be provided to share with users what the new update is about.  It should probably be more specific than the example below.

```
git commit -m "update file"
```
* Use `git push` to push your committed version of the file to the remote repository.
```
git push
```

Did it work? Re-load your github webpage and navigate to the README.md file. Do you see your edits?

##5.  Writing workflows in Markdown for use on GitHub

How do we create these helpful tutorials on github, with headers, links, images, etc? Markdown!

* Markdown is a syntax for fast text-to-html conversion so that it is readable and web-ready.
* The extension of a markdown document is ".md".  GitHub will automatically render documents with .md extension to be pretty on the web interface.
* You can use any text editor to write a mark down document.  Two nice open ones are [sublime](http://www.sublimetext.com/) and [atom](https://atom.io/).
* Take a look a this document "raw" to have an exampe of what markdown looks like without rendering.
* Here is one [cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) for Markdown syntax; there are many!
* _Fun Exercise!_ : Create a markdown document and post it to a new GitHub repository that you've created.

***
##Help and other resources
* GitHub [Glossary](https://help.github.com/articles/github-glossary/) of Git terms and jargon.
* GitHub has a [Bootcamp](https://help.github.com/categories/bootcamp/) series of tutorials for getting started.
* GitHub curated page of [learning resources](https://help.github.com/articles/good-resources-for-learning-git-and-github/)
* At the bottom of all GitHub documentation, there is an button to[Contact a Human](https://github.com/contact)
* [Markdown](http://daringfireball.net/projects/markdown/) documentation and official site.
