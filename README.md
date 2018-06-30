Vim - the text editor - for Mac OS X

- MacVim homepage http://macvim-dev.github.io/macvim
- Vim README https://github.com/macvim-dev/macvim/blob/master/README_vim.md
- [Cumstom Build](https://github.com/macvim-dev/macvim/wiki/Building-(not-recommended-way))


## Build
1. `cd src`
1. `./configure --with-features=huge --enable-rubyinterp --enable-perlinterp --enable-python3interp --with-python3-config-dir=MY_PYTHON3_CONFIG_DIR`
1. `make`

#### How to find MY_PYTHON3_CONFIG_DIR
If you are using python3.4: `python3.4-config --configdir`

You will get like this path: `/usr/local/opt/pyenv/versions/3.4.3/lib/python3.4/config-3.4m`

#### Resolve error while running `make` command
If you get this error:
```
ERROR: xcode-select: error: tool 'xcodebuild' requires Xcode, but active developer directory '/Library/Developer/CommandLineTools' is a command line tools instance
```
then,
1. run XCode
1. open Preferences > Locations
1. Select an item in `Command Line Tools`


## Run
`cd MacVim/build/Release/MacVim.app`
### run in terminal
1. run
   ```
   ln -s /Applications/MacVim.app/Contents/bin/mvim /usr/local/bin/mvim
   ```
1. set alias in your shell rc file like `~/.zshrc`:
    ```
    alias vi="/usr/local/bin/mvim"
    ```

reference https://github.com/macvim-dev/macvim/wiki/FAQ


## VIMRC
- example: https://github.com/dokenzy/vimrc
### font
To use webdevicon with airline-powerline, set like this:
```set guifont=Roboto\ Mono\ Light\ Nerd\ Font\ Complete\ Mono:h13```

this requires customized font. Download and install you want: https://github.com/dokenzy/nerd-fonts
