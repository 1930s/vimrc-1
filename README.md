# My Tiny Vim Configuration

This is my vim configuration for my daily programming usage. I configured my vim to be programming-friendly with suitable tweaks to built-in features, interface, formatting, etc. The plugins I choose tend to be simple-to-use and practical. I don't mean to make a completely different editor or to make a fancy vim so I would keep everything simple and won't go far from typical vim practices.

I will update it from time to time. Feel free to clone/fork it if you find my configuration suitable for you.

GitLab (Main): https://gitlab.com/archerindigo/vimrc

GitHub (Mirror): https://github.com/archerindigo/vimrc

# Table of Content
1. [Featurs and Objectives](#feature-and-objectives)
2. [Screenshots](#screenshots)
3. [Plugins Included](#plugins-included)
4. [Color Schemes Included](#color-schemes-included)
5. [Installation](#installation)
6. [Usage Tips](#usage-tips)

## Features and Objectives

__Objectives:__
* To provide nicer but remain simple interface
* To include simple-to-use and practical plugins
* To provide a programming-friendly environment

__Major features included:__
* Interface settings for more comfortable coding
* Formatting that match general programming standard
* Easier code exploration and navigation
* Easier file navigation
* Simple session save/load
* Support of git

You may look into .vimrc to better understand what have set.

## Screenshots
![2 C++ files with tabs, nerdtree and taglist in gvim](/screenshots/0.3.0-1.png)
2 C++ files with tabs, nerdtree and taglist opened in gvim

![A markdown file opened in transparent terminal](/screenshots/0.3.0-2.png)
A markdown file opened in a transparent terminal

More in screenshots folder.

## Plugins Included

* [vim-plug](https://github.com/junegunn/vim-plug): A easy-to-use plugin manager.
* [lightline.vim](https://github.com/itchyny/lightline.vim): A light-weight but good-looking and powerful enough status line replacement.
* [NERDTree](https://github.com/scrooloose/nerdtree): A tree-view file explorer.
* [nerdtree-git-plugin](https://github.com/Xuyuanp/nerdtree-git-plugin): A extension on top of NERDTree providing git status flags in the file explorer.
* [taglist](https://github.com/vim-scripts/taglist.vim): Provides overview of the structure of the code.
* [fugitive.vim](https://github.com/tpope/vim-fugitive): A git wrapper
* [gitv](https://github.com/gregsexton/gitv): A repository viewer similar to gitk. Based on fugitive.

## Color Schemes Included

* [wombat256i](https://github.com/dsolstad/vim-wombat256i): My default scheme for vim. The dim but colorful syntax highlight could make you differentiate the components of your code easily. It also supports transparent background in terminal.
* [wombat](https://github.com/vim-scripts/Wombat): My default scheme for gvim.
* [jellybeans](https://github.com/nanotech/jellybeans.vim): Another dark and even more colorful scheme.
* [molokai](https://github.com/tomasr/molokai): A dark scheme but has higher contrast.
* [peaksea](https://github.com/vim-scripts/peaksea): This scheme is dark in background but light in syntax.

## Installation

1. Clone the repository:

Third-party repositories are included in this repository. Remember to use --recursive to pull them all!
<pre>
git clone --recursive https://gitlab.com/archerindigo/vimrc.git
</pre>

2. Replace your ~/.vimrc and ~/.vim

<pre>
cp vimrc/.vimrc ~
cp -r vimrc/.vim/* ~/.vim/
</pre>

The configuration will be applied to local profile only. If you want to make it take effect system-wide (e.g. take effect in sudo vim), you should copy the content of .vimrc to /etc/vim/vimrc

## Usage Tips

Here are some customized usage in my configuration:

### Transparent Background

The wombat256i color scheme supports transparent background in 256-color so you can use vim with transparent background in terminal.

### Switching Tab

You can use __Ctrl-Up__ and __Ctrl-Down__ to switch between tabs. They works in normal mode only for safety.

### Save and Load Session

You can save session by pressing __F2__ and then type the file name. To load a session, you can press __F3__ and type the file name. The default storage is __~/.vim/sessions/__ .

### Toggle NERDTree

Press __Ctrl-G__ to toggle NERTree's explorer

### Toggle taglist

Press __F8__ to toggle taglist

### Copy and Paste to System Clipboard

You can select text in visual mode and press __Ctrl-C__ to copy or __Ctrl-X__ to cut it into system clipboard. To paste the text, you can press __Ctrl-P__ in normal mode or __Ctrl-V__ in insert mode.

### Recommended font

It is recommended to use __Source Code Pro__ size 10 as the font. You can uncomment __"set guifont=Source\ Code\ Pro\ 10"__ in .vimrc to enforce the font in gvim. For vim you should set the terminal font by yourself.

## Troubleshooting

### Taglist: Exuberant ctags (http://ctags.sf.net) not found in PATH. Plugin is not loaded.__

Reason: ctags is missing
<pre>sudo apt-get install ctags</pre>
