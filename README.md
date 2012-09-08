# Introduction

Git does not support a side-by-side diff option. This script generates a side-by-side git-diff output for terminals.

# Usage

The tool supports two modes:

* `stdin`: Pipe the git-diff output to the script:

    $ git diff | ssdiff

* `GIT_EXTERNAL_DIFF`: 

    $ GIT_EXTERNAL_DIFF=ssdiff git diff

or

    $ git difftool --extcmd=ssdiff

# Configuration

No parametrized configuration exists yet. In the script one can adopt the theme:

* **none**: No colors for hunks

* **normal**: Default, red and green text color for hunks

* **light**: Red and green text color and white background for hunks

* **dark**: Red and green text color and black background for hunks

* **bold**: black text color and red and green background for hunks
