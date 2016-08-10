Vim Frontend: a Vim configured for Front-end Developers.
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
    - [Learning Vim](#learning-vim)
        - [Super Fast Navigation](#super-fast-navigation)
    - [HTML Commands](#html-commands)
    - [JavaScript Commands](#javascript-commands)
        - [JavaScript ES6 React](#javascript-es6-react)
        - [AngularJS 1 e 2](#angularjs-1-e-2)
    - [CSS Commands](#javascript-commands)
    
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
git clone https://github.com/VictorVoid/vim-frontend.git
mv vim-frontend/.vimrc ~/ && mv vim-frontend/autoload/ ~/.vim && mv vim-frontend/ultisnips/ ~/.vim
```

or

```bash
- Download ZIP
cd /Users/yourusername/Download
- Open terminal
unzip vim-frontend-master.zip
mv vim-frontend/.vimrc ~/ && mv vim-frontend/autoload/ ~/.vim && mv vim-frontend/ultisnips/ ~/.vim
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

    git clone https://github.com/VictorVoid/vim-frontend.git
    mv vim-frontend/.vimrc ~/ && mv vim-frontend/autoload/ ~/.vim && mv vim-frontend/ultisnips/ ~/.vim

or

    - Download ZIP
    cd /Users/yourusername/Download
    - Open terminal
    sudo apt-get install unzip
    unzip file.zip -d
    mv vim-frontend/.vimrc ~/ && mv vim-frontend/autoload/ ~/.vim && mv vim-frontend/ultisnips/ ~/.vim
    
    
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

- Automatic syntax and codestyle checks.
- JavaScript autocomplete ([ternjs](http://ternjs.net/))
- HTML with auto close tag
- Integration with Git
- Emmet
- Snippets
- TagBar (overview of its structure)
- Vim Session (restore your Vim editing sessions)
- Surround (provides mappings to easily delete, change and add such surroundings in pairs)
- Integration with CSS Pre-processors (SASS, LESS and Stylus)
- Color preview (css/less/sass/html)
- Beautify (HTML, CSS, JS)

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


Learning Vim
------------

You can learn basic vim here: 

* [The 11 Steps to Learning Vim](https://github.com/damassi/learn-vim)
* [The 30 Basic Vim Commands You'll Use Every Day](https://spin.atomicobject.com/2016/04/19/vim-commands-cheat-sheet/)
* [Vimbook (in portuguese)](https://cassiobotaro.gitbooks.io/vimbook/content/)
* [Vim para noobs (in portuguese)](https://woliveiras.com.br/vimparanoobs/)
* [VIM Editor Commands ](http://www.radford.edu/~mhtay/CPSC120/VIM_Editor_Commands.htm)

### Super Fast Navigation

Commands | Descriptions
--- | ---
`e` | Move to the end of a word
`w` | :arrow_right: Move forward to the beginning of a word ->
`W` | :arrow_right: Move forward a WORD (any non-whitespace characters)
`b` | :arrow_left: Move backward to the beginning of a word
`(` | :arrow_down: Jump backward one sentence
`)` | :arrow_up: Jump forward one sentence.
`3w, 3b` | :left_right_arrow: Move forward three words, Move backward three words
`$` | Move to the end of the line
`0"` | Move to the beginning of the line
`H` | Jump to the top of the screen
`M` | Jump to the middle of the screen
`L` | Jump to the bottom of the screen
`mx` | Set mark x at the current cursor position
`'x` | Jump to the beginning of the line of mark x
``x` | Jump to the cursor position of mark x

HTML Visual Navigation | Descriptions
--- | ---
`at` | Select the outer tag block by pressing
`it` | Select the inner tag block



HTML Commands
------------

[![asciicast](https://asciinema.org/a/80816.png)](https://asciinema.org/a/80816)

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

**Navigating HTML tags in Vim**

1. Enter visual mode
2. Select the outer tag block by pressing  **a** + **t** or **i** + **t** for inner tag block.

- [Video demonstration](https://asciinema.org/a/80816)
- [Emmet Cheat Sheet](http://docs.emmet.io/cheat-sheet/)
- [Vim-surround](https://github.com/tpope/vim-surround)

JavaScript Commands
-------------------

### JavaScript ES6 React
[![asciicast](https://asciinema.org/a/80829.png)](https://asciinema.org/a/80829)

**vf**

```js
var functioname = function (arg){
    //
}
```

**

```js
/**
*
**/
```

**ex**

```js

module.exports = yourmod

```

**css**

```js

{yourobj}.css('atribuite', 'value')

```

**qs**

```js

document.querySelector('selector')

document.querySelectorAll('selector') //qsa

```

**trf**

```js

try {

} catch (e) {

} finally {

}
```

**proto**

```js

class_name.prototype.method_name = function(){
    
}
```

**props**

```js

var my_object = Object.defineProperties{
    new Object(),
    {
        property: {
            get: function my_object_property_getter(){
            
            },
            set: function my_object_property_setter(value){
            
            },
            value       : value,
            writeable   : boolean,
            enumerable  : boolean,
            configurable: boolean
        }
    }
}
```

**us**

```js
'use strict';
```

**=>**

```js

( ) => {

}

```

**cla**

```js

Class classname{


}
```

**clax**


```js
Class classname extends classname{

}

```

**imp**

```js
import ModuleName from 'ModuleName'

```


**cc**


```js

const app = React.createClass({
    render: function(){
    
    }
})

```


**cdm**


```js

componentDidMount: function(){

},

```


**gis**


```js
getInitialState: function(){
    return {
    
    };
},
```

- [Video demonstration](https://asciinema.org/a/80829)
- [More information about Snippets](https://github.com/honza/vim-snippets)

### AngularJS 1 e 2

[![asciicast](https://asciinema.org/a/81384.png)](https://asciinema.org/a/81384)

Commands | Directive
--- | ---
`na` | ng-app=""
`nc` | ng-click=""
`nctrl` | ng-controller=""
`ncl` |  ng-class=""
`nm` | ng-model=""
`ns` | ng-show=""
`nh` | ng-hide=""
`nb` | ng-bind=""
`{{` | {{}}
`n2c` | (click)=""
`n2dbc` | (dblclick)=""
`n2ctrl` | ngController=""
`n2m` | [(ngModel)]=""
`n2cl` | [ngClass]=""

**ngsa**
```html
 <script src="https://ajax.googleapis.com/ajax/libs/angularjs/x.x.xx/angular.js"></script> 
```

**$v**
```js
$scope.variable = value;
```

**ngc**
```js
var controllerName = function(scope, injectables){

};
```

**ngfor**
```js
angularforEach(iterateOver, function(value, key){
    
});
```

**ngm**
```js
angular.module('moduleName', [moduleDependencies]);
```

**ngma**
```js
var moduleName = angular.module('moduleName', [moduleDeps]);
```

**ngmfa**
```js
factory('factoryName', function(dependencies){

});
```

**ngms**
```js
service('serviceName', function(injectables){

});
```

**ngmfi**
```js
filter('filterName', function(injectables){
    return function(inputs, args){
    
    };
});
```

**ngrwr**
```js

$routeProvider.when('url', {
    templateUrl: 'templateUrl',
    controller: 'controller',
    resolve: {
    
    }
});

```

**ngro**
```js
$routeProvider.otherwise({
    redirectTo: 'url'
});
```

**TypeScript**:

Snippets from [Martin Prins](https://github.com/magarcia/vim-angular2-snippets)

```typescript
ng2-component-root  // Angular 2 root App component
ng2-bootstrap     // Angular 2 bootstraping, for main.ts
ng2-component     // Angular 2 component
ng2-pipe          // Angular 2 pipe
ng2-route-config  // Angular 2 @RouteConfig
ng2-route-path    // Angular 2 routing path
ng2-service       // Angular 2 service
ng2-subscribe     // Angular 2 observable subscription
```

CSS Commands
-------------------

[CSS Abbreviations](http://docs.emmet.io/css-abbreviations/)
