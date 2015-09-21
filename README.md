Mix completion plus shortcuts and colors
========================================

Bash autocompletion for Elixir [mix](http://elixir-lang.org/getting-started/mix-otp/introduction-to-mix.html).

Don't forget to check the **power feature(s)** on the bottom.

## Installation

Global:

    $ git clone git@github.com:davidhq/mix-power-completion.git
    $ cd mix-power-completion
    $ sudo cp mix /etc/bash_completion.d/
    $ . /etc/bash_completion.d/mix
    (on new terminal tabs, this should be autoloaded)

Local:

    $ ~/bash_completion.d
    $ cp mix ~/bash_completion.d/

Add to `~/.bashrc`:

    if [ -f "$HOME/bash_completion.d/mix" ] ; then
        . $HOME/bash_completion.d/mix
    fi
    . ~/bash_completion.d/mix

## Brew completions

This will hopefully be included [here](https://github.com/Homebrew/homebrew-completions) soon...

## Usage

To list mix tasks:

    $ m [TAB]
      archive            archive.uninstall  compile            deps.clean         deps.unlock      ....

To complete command:

    $ m t[TAB]
    $ m test

There is a slight lag before completion because mix has to check what is available for current project.

You can also use the normal `mix` command here instead of `m` (but the features below won't work).

## Power features

### Shortcuts

You can invoke tasks in a shorter way without pressing `TAB`:

    m      → mix help
    m a    → mix archive
    m h    → mix hex
    m a.b  → mix archive.build
    m d.co → mix deps.compile
    m p.n  → mix phoenix.new

### Colorize

When you execute `m` (or `m help`), tasks are colored green.
