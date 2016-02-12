# Introduction

Git does not support a side-by-side diff option. This script generates a
side-by-side git-diff output for terminals. The script uses the maximum terminal
width for the diff output.

Works well with [diff-highlight](https://github.com/git/git/tree/master/contrib/diff-highlight).


# Usage

The tool supports two modes:

* `stdin`: Pipe the git-diff output to the script:

    $ git diff | {PATH}/diff-ss

* `GIT_EXTERNAL_DIFF`:

    $ GIT_EXTERNAL_DIFF={PATH}/diff-ss git diff

or

    $ git difftool --extcmd={PATH}/diff-ss

or

    alias -r gd = '_() { git diff $@ | diff-ss }; _'


# Configuration

No parametrized configuration exists yet. In the script one can adopt the theme:

* **none**: No colors for hunks

* **normal**: Default, red and green text color for hunks

* **light**: Red and green text color and white background for hunks

* **dark**: Red and green text color and black background for hunks

* **bold**: black text color and red and green background for hunks


# Screenshots

![Example: Normal](https://github.com/djui/git-ssdiff/raw/master/example_normal.png)
