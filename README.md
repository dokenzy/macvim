Vim - the text editor - for Mac OS X

- MacVim homepage http://macvim-dev.github.io/macvim

- Vim README https://github.com/macvim-dev/macvim/blob/master/README_vim.md


## Build
1. `cd src`
1. `./configure --with-features=huge --enable-rubyinterp --enable-perlinterp --enable-python3interp --with-python3-config-dir=MY_PYTHON_CONFIG_DIR`
1. `make`

#### How to find MY_PYTHON_CONFIG_DIR
If you have installed python 3.4 with brew,run this command in terminal:

```/usr/local/opt/pyenv/shims/python3.4m-config --configdir```

You will get like this path: ```/usr/local/opt/pyenv/versions/3.4.3/lib/python3.4/config-3.4m```
