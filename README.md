# CTRL-VIM & FRIENDS

I use this directory in order to quickly set up my linux environment on other computers. Anyone is welcome to copy this configuration including my .bashrc.

* These tools assume you are using Ubuntu 16.04

* There are some useful tools and aliases in .bashrc

* You do not need my .bashrc to use ctrl-vim. You only need to use my .vimrc. You may need to add a line to your existing .bashrc.. my install script appends this line to the end of your .vimrc automatically.

* TODO: add an option to toggle code-completion options using commented-out plugins

![alt text](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSP_T4R2Mnc8ja4jZ5pIBk0jlk7enzbcN3VeAFO52-QA3UpABlx)

## CTRL-VIM
* I give you a simplified and expanded vim IDE defined by my .vimrc file. 
* There are shortcuts that make vim a lot easier to use without having to enter many characters to do things like opening files, splitting tabs, etc.
* I broke some of the basic vim functionality in order to make these hotkeys work

* Navigation

      Ctrl+a (or ESCAPE)       - enter normal mode
      Space  (normal mode)     - toggle center-scroll
      v  (normal mode)         - toggle visual mode
      Shift+v  (normal mode)   - enter visual-line mode
      ; (normal mode)          - enter command mode
      a (normal mode)          - enter insert mode
      ' (normal mode)          - run bash command via ':! <command>' (this one is awesome)
      Alt+Left/Right           - next/previous location
      Alt+Up/Down              - go up or down 10 lines at a time
      Ctrl+Left/Right/Up/Down  - move between windows
      Shift+Left/Right         - move between tab pages
      Shift+Up/Down            - equal to page up/page down
      ge                       - go to end of line (excluding training whitespace)
      gs                       - go to start of line (excluding training whitespace)
      gf                       - go to first non-whitespace char in previous line
      Ctrl+t                   - toggle mouse 
      Ctrl+l                   - toggle line numbers
      Ctrl+j+j+j               - (re)generate ctags for current working directory (be careful not to do this by accident!)
      Shift+j                  - jump to the definition of func/variable under cursor if exists, or show all definitions
      jj                       - (smart) jump to definition of function/variable under cursor (requires prior ctag gen)

* Windows and Tabs

      Ctrl+b+enter             - create a new tab
      Ctrl+n                   - create a vertically split window
      Ctrl+y                   - create a horozontally split window
      b+{qwerty} (normal mode) - bookmark the file in the current window to one of {qwerty}
      Shift+{qwerty} ("""")    - jump to {qwerty} bookmark
      Shift+s (normal mode)    - switch background color  
      Shift+b                  - show all bookmarks

* Files and Directories

      Ctrl+s                   - save changes to current file
      Ctrl+q                   - attempt to save changes to file in current window and quit
      Shift+z+z+z (normal mode)- force close all windows without saving
      Shift+s+s+s (normal mode)- force close all windows and save if possible
      Ctrl+e                   - open a file in the current window
      Ctrl+b                   - open a file in a new tab
      Ctrl+g                   - open nerdtree showing current file (no cursor switch)
      ls (normal mode)         - open nerdtree showing current working directory
      cd (normal mode)         - change current working directory to that specified
      cc (normal mode)         - show current working directory
      Shift+c (normal mode)    - change current working directory to file in current window   
      Shift+x (normal mode)    - change write permissions of current file
      Shift+b (normal mode)    - refresh buffers


* Basic Editing

      cw                       - copy word to regular copy buffer
      cl                       - copy line to regular copy buffer
      kk                       - copy line/selection to kappa buffer
      kw                       - copy word to kappa buffer
      kl                       - copy line to kappa buffer
      Ctrl+k                   - paste contents of kappa buffer
      Ctrl+d (insert mode)     - autocomplete word/function/variable name
      Ctrl+p                   - autocomplete word/function/variable name 
      dd                       - delete
      Ctrl+w                   - write a newline from normal mode
      Ctrl+c                   - yank (to regular buffer)
      Ctrl+v                   - paste what is yanked
      Ctrl+z                   - undo
      Ctrl+r                   - redo
      Ctrl+u (insert mode)     - toggle special paste insert mode for when copying from outside of vim
      Tab                      - indent
      Shift+Tab                - unindent
      ,c+Space (normal mode)   - toggle block comments
      Shift+k  (normal or vis) - copy selected text to kappa buffer (wont be overwritten by Ctrl+c)
      Ctrl+k (any mode)        - paste text in kappa buffer
      di"                      - delete contents between quation marks and place cursor there
      di(                      - delete contents between parens and palce cursor there
      di{                      - delete contents between braces and place cursor there
      #d (normal mode)         - print a block comment line /***...***/


* Easy Repeated Actions

      gg                       - start recording keystrokes (using register g)
      q                        - stop recording keystrokes (using register g)
      Shift+g                  - executed recorded keystrokes (using register g)

* Search Tools

      ...Note that even though multi-file search looks like it is using Ack!, it really uses ag
     
      ff                       - find the word under the cursor (in current file)
      /<text>                  - find text in file in current window
      n (normal mode)          - go to next instance of found text
      Shift+n (normal mode)    - go to prev instance of found text
      * (normal mode)          - start a new search for text under cursor (in current file) 
      Shift+d (normal mode)    - find text in all files under current working directory (cwd)
      Ctrl+d (normal mode)     - find text in files in cwd where filename matches pattern 
      Ctrl+f                   - fuzzy filename search (Ctrl+p)
      Shift+f (normal mode)    - find and replace text in file in current window
      Shift+h                  - toggle search highlighting
      Ctrl+h                   - search through/run vim command history (includes all searches and files)

* Advanced

      :make                    - run make and capture output
      :cn                      - jump to file containing make error
      :cc                      - show make error message
      Ctrl+i                   - toggle syntastic syntax error checking in file
      
* Miscellaneous
    
      I constantly update this .vimrc...
      ...you may find that a hotkey is broken or has been remapped to something else
      ...you may also find new goodies
      , is the leader key
      f controls various easymotion things besides what I remapped
      c controls various commenting functions from nerdcommenter
      I clobbed a lot of regular hotkeys in order to make this usable for me
      If you hate what I did, feel free to change whatever you want
      If you have suggestions, let me know

* Help
     
      :help                  - view general help
      :help <key-combo>      - see what default vim commands I clobbered for the key sequence specified
      :help nerdcommenter    - view commenting plugin help
      :help nerdtree         - view file searching help
      :help easymotion       - view navigation plugin help
      :help ctrlp            - view help for fuzzy file searching
      :help ack              - view help for ack multi-file search (not accurate if silversearcher-ag is installed which it is by my script)

* Gnome-Terminal Fun (vim and terminal are designed to be used together. do it.)
      
      Ctrl+Shift+t           - create a new terminal tab
      Ctrl+[PageUp/PageDown] - switch between terminal tabs
      Alt+[number]           - jump to terminal tab # [number]



* I believe that people should get credit for making the internet a better place. Many props to Sebastian Karlson from whom the vim stuff on this page has been copied and tweaked (https://github.com/sebbekarlsson)

## Installing CTRL-VIM

* Run the following commands

      git clone https://github.com/mikedefrancis/ctrl-vim ctrl-vim
      cd ctrl-vim
      ./install_ctrl_vim
      source ~/.bashrc

* The install script only works with ubuntu

* If you encounter problems running the install script, please perform the following steps:
      
      git clone https://github.com/mikedefrancis/ctrl-vim ctrl-vim
      gcd ctrl-vim
      sudo apt-get install vim silversearcher-ag exuberant-ctags   
      mkdir -p ~/.vim/bundle
      git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
      echo 'stty -ixon' >> ~/.bashrc
      p .vimrc ~/.vimrc
      vim -c ":PluginInstall" -c ":qa!" README.md
      source ~/.bashrc
      

* theoreticaly this work on other linuxes besides ubuntu but this has not been tested

* see https://www.youtube.com/watch?v=zF9EcpYb1KE for details using vundle and vim

## OPTIONAL: install i3

          sudo apt-get install i3

* there are better ways to install and configure i3, but this works on ubuntu

* logout, select i3 as the desktop, and log back in. for a tutorial on using i3, see:

* https://fedoramagazine.org/getting-started-i3-window-manager/


## REFERENCE

* Vim Cheatsheet For Programmers (note that I broke some of these hotkeys and may consider restoring their functionality later)

![alt text](http://michael.peopleofhonoronly.com/vim/vim_cheat_sheet_for_programmers_screen.png)


