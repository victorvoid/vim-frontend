Vim Frontend: a .vimrc configured for Front-end Developers.
===========================================================

- [Installation](#installation)
    - [Mac OS X](#mac-os-x)
    - [Linux x64](#linux-x64)
- [Quick Feature Summary](#quick-feature-summary)

Installation
------------

### Mac OS X

*Pre-requisite*:
```
$ brew install git ctags
```
**Just replace your .vimrc :shipit:**

    cd ~ 
    git clone https://github.com/VictorVoid/vim-frontend.git .
    vim
    
or

    Download ZIP
    cd /Users/yourusername/Download
    unzip vim-frontend-master.zip
    cp vim-frontend-master/.vimrc ~/
    
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

Quick Feature Summary
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
