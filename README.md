Vim Frontend: a .vimrc configured for Front-end Developers.
===========================================================
![Licence](https://img.shields.io/badge/licence-MIT-red.svg?style=flat)
![asciinema](https://img.shields.io/badge/asciinema-demos-brightgreen.svg)

- [Introduction](#introduction)
- [Installation](#installation)
    - [Mac OS X](#mac-os-x)
    - [Linux x64](#linux-x64)
- [Features Summary](#features-summary)
- [User Guide](#user-guide)
    - [General Commands](#general-commands)
    - [HTML Commands](#html-commands)
    
Introduction
------------

Is you a Front-end Developer ? Are you using Sublime Text, Atom, Brackets, Visual Studio Code or anything ?

> "Give me a chance. Don't worry, I'm easy :smile: " - Vim

[Quick demo videos](https://asciinema.org/~victorvoid)

Installation
------------

### Mac OS X

*Pre-requisite*:
```
$ brew install git ctags
```
**Just replace your .vimrc :shipit:**

```bash
git clone clone https://github.com/VictorVoid/vim-frontend.git
mv vim-frontend/.vimrc ~/
```

or

```bash
cd ~ 
git clone https://github.com/VictorVoid/vim-frontend.git .
vim
```

or

```bash
Download ZIP
cd /Users/yourusername/Download
unzip vim-frontend-master.zip
mv vim-frontend-master/.vimrc ~/
```
    
*YouCompleteMe Plugin INFO:* :ear:

**Remember:** YCM is a plugin with a compiled component. If you **update** YCM
using Vundle and the ycm_core library APIs have changed (happens
rarely), YCM will notify you to recompile it. You should then rerun the install
process.

Don't worry, it's easy :smile: Let's go.

Install [Homebrew](http://brew.sh/)

    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

Install cmake via Homebrew

    brew install cmake
    
Compiling YCM **with** semantic support for C-family languages:

    cd ~/.vim/bundle/YouCompleteMe
    ./install.py --clang-completer
    
[More info](https://github.com/Valloric/YouCompleteMe)

### Linux x64
*Pre-requisite*:
* Ubuntu\Debian

```
$ sudo apt-get install git exuberant-ctags ncurses-term python-jinja2
```

* Gentoo
```
$ sudo emerge dev-util/ctags sys-libs/ncurses dev-vcs/git dev-python/pyflakes dev-python/jinja
```

* Arch Linux via *pacman* (recomend used *pacaur*)
```
$ sudo pacman -S git-core ctags ncurses python-jinja
```
* Fedora

```
$ sudo dnf install ncurses-devel git ctags-etags
```

**Just replace your .vimrc :shipit:**

    git clone clone https://github.com/VictorVoid/vim-frontend.git
    mv vim-frontend/.vimrc ~/

or

    cd ~ 
    git clone https://github.com/VictorVoid/vim-frontend.git .
    vim
    
or

    Download ZIP
    cd /Users/yourusername/Download
    sudo apt-get install unzip
    unzip file.zip -d
    cp vim-frontend-master/.vimrc ~/
    
    
*YouCompleteMe Plugin INFO:* :ear:

**Remember:** YCM is a plugin with a compiled component. If you **update** YCM
using Vundle and the ycm_core library APIs have changed (happens
rarely), YCM will notify you to recompile it. You should then rerun the install
process.

Install development tools and CMake: `sudo apt-get install build-essential cmake`

Make sure you have Python headers installed: `sudo apt-get install python-dev
python3-dev`.

Compiling YCM **with** semantic support for C-family languages:

    cd ~/.vim/bundle/YouCompleteMe
    ./install.py --clang-completer
    
[More info](https://github.com/Valloric/YouCompleteMe)

Features Summary
-----

- Syntax highlighting :white_check_mark:
- JavaScript autocomplete ([ternjs](http://ternjs.net/)) :white_check_mark:
- ES6 Snippets :white_check_mark:
- HTML with auto close tag :white_check_mark:
- Git Support :white_check_mark: 
- Emmet :white_check_mark:
- TagBar (overview of its structure) :white_check_mark:
- Vim Session (restore your Vim editing sessions) :white_check_mark:
- Surround (provides mappings to easily delete, change and add such surroundings in pairs) :white_check_mark:
- Support CSS Pre-processors (SASS, LESS and Stylus) :white_check_mark:
- Color preview (css/less/sass/html) :white_check_mark:
- Beautify (HTML, CSS, JS) :white_check_mark:

User Guide
------------

### General Commands

Have you ever used this [Generator](http://vim-bootstrap.com/)(Vim Bootstrap) ? The General commands is the same thing, you don't need learning others. :bowtie:

General Commands | Descriptions
--- | ---
`:cd <path>` | Open path */path*
`<Control+w>+<hjkl>` | Navigate via split panels
`<Control>+w+w` | Alternative navigate vim split panels
`,.` | Set path working directory
`,w or ,x` | Next buffer navigate
`,q or ,z` | previous buffer navigate
`SHIFT+t` | Create a tab
`TAB` | next tab navigate
`SHIFT+TAB` | previous tab navigate
`,e`  | Find and open files
`,b`  | Find file on buffer (open file)
`,c`  | Close active buffer (clone file)
`F2`  | Open tree navigate in actual opened file
`F3`  | Open/Close tree navigate files
`F4`  | List all class and method, support for python, go, lua, ruby and php
`,v`  | Split vertical
`,h`  | Split horizontal
`,f`  | Search in the project
`,o`  | Open github file/line (website), if used git in **github**
`,sh` | Open shell.vim terminal inside Vim or NeoVim built-in terminal
`,ga` | Execute *git add* on current file
`,gc` | git commit (splits window to write commit message)
`,gsh`| git push
`,gll`| git pull
`,gs` | git status
`,gb` | git blame
`,gd` | git diff
`,gr` | git remove
`,so` | Open Session
`,ss` | Save Session
`,sd` | Delete Session
`,sc` | Close Session
`>`   | indent to right
`<`   | indent to left
`gc`  | Comment or uncomment lines that {motion} moves over
`YY`  | Copy to clipboard
`,p`  | Paste
`<Control+y>,` | Activate Emmet plugin

HTML Commands
------------

Commands | Descriptions
--- | ---
`html5+<tab>` | snippet html tree
`css+<tab>` | snippet link css
`ysiw` | wrap tag in word
`yss` | wrap the entire line
`cst <updatetag>` | change tag to update tag
`cs"'` | change " to '
`ds"` |  remove the delimiters entirely
`dst"` |  remove the delimiters entirely (t == tag)

- [Video demonstration](https://asciinema.org/a/80816)
- [Emmet Cheat Sheet](http://docs.emmet.io/cheat-sheet/)
- [Vim-surround](https://github.com/tpope/vim-surround)
