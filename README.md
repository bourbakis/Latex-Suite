# Latex-Suite
This guide and templates are parsed from http://vim-latex.sourceforge.net/ and https://sharelatex.com.
If more information for Latex-Suite are needed, visit above site.

## What is latex-suite?
Latex-Suite attempts to provide a comprehensive set of tools to view, edit and compile LaTeX documents in Vim. Together, they provide tools starting from macros to speed up editing LaTeX documents to functions for forward searching .dvi documents. Latex-Suite is released under the Vim charityware license. The current copyright holders of Latex-Suite are Srinath Avadhanula and Mikolaj Machowski.

Latex Suite is vim-version independent plugin so it can be used on any vim such as vim-gtx, vim-gnome and vim-basic.
The plugin only started when user open .tex file. Thus, the user can use vim with no changes.

## Installation Guide
This installation guide refers http://vim-latex.sourceforge.net/index.php?subject=download&title=Download. The installation guide only targets Ubuntu 16.04, and installation is confirmed only with ubuntu 16.04. In addition, if you are using another plugin, then refer this: http://vim-latex.sourceforge.net/index.php?subject=download&title=Download#advanced

### Step 1 of 4: Download and extract the archives
https://sourceforge.net/projects/vim-latex/files/
Extract one of the archives above into ~/.vim directory.
If you are updating after a long time, it might be a good idea to remove the ~/vimfiles/ftplugin/latex-suite directory from previous installations before reinstalling.

### Step 2 of 4: Set a few things in .vimrc
Write this on your .vimrc file.
If you are reading this, it most probably means that you have already installed Latex-Suite and the help files.
Make sure that you create a few necessary settings in your ~/.vimrc.

```
" REQUIRED. This makes vim invoke Latex-Suite when you open a tex file.
filetype plugin on

" IMPORTANT: win32 users will need to have 'shellslash' set so that latex
" can be called correctly.
set shellslash

" OPTIONAL: This enables automatic indentation as you type.
filetype indent on

" OPTIONAL: Starting with Vim 7, the filetype of empty .tex files defaults to
" 'plaintex' instead of 'tex', which results in vim-latex not being loaded.
" The following changes the default filetype back to 'tex':
let g:tex_flavor='latex'
```

In addition, the following settings could go in your ~/.vim/ftplugin/tex.vim file:

```
" this is mostly a matter of taste. but LaTeX looks good with just a bit
" of indentation.
set sw=2
" TIP: if you write your \label's as \label{fig:something}, then if you
" type in \ref{fig: and press <C-n> you will automatically cycle through
" all the figure labels. Very useful!
set iskeyword+=:
```

### Step 3 of 4: Install the help files
To install the included latex-suite.txt and latexhelp.txt files as vim help files, start vim and do the following:

``helptags ~/.vim/doc``

### Step 4 of 4: Done!
Thats it! You are done! Now start editing a latex file in vim. Latex-Suite should start up automatically. You can do

``:help latex-suite.txt``

### Additional comment
Remember, Latex-Suite is simply a set of utilities meant to work with Vim. Installing Latex-Suite does not mean that LaTeX is installed. You will need to install LaTeX seperately.

## Commands
Making Latex-Suite commands guide are on progressing. Before completion, refer this link: https://docs.google.com/presentation/d/1j-4IiNXm24r10gczn5yGuc9Nq1-w2EU_QzlKsvUM9lo/edit?usp=sharing
