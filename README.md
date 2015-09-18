Mix Bash completion with extra goodies
======================================

Bash autocompletion for Elixir [mix](http://elixir-lang.org/getting-started/mix-otp/introduction-to-mix.html).

Don't forget to check the **power feature** on the bottom.

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
    $ echo "" >> ~/.bashrc
    $ echo 'if [ -f "$HOME/bash_completion.d/mix" ] ; then' >> ~/.bashrc
    $ echo '    . $HOME/bash_completion.d/mix' >> ~/.bashrc
    $ echo "fi" >> ~/.bashrc
    $ . ~/bash_completion.d/mix

## Brew completions

This will hopefully be included [here](https://github.com/Homebrew/homebrew-completions) soon...

## Usage

To list mix tasks:

    $ m [TAB]
      archive            archive.uninstall  compile            deps.clean         deps.unlock      ....

To complete command:

    $ m t[TAB]
    $ m test

There is a slight lag before completion because mix has to check what is available in current directory.

You can also use the normal `mix` command here instead of `m` (but the feature below doen't work with it and it doesn't make sense because we want the shortest command possible).

## Power feature

You can invoke commands in a shorter way without pressing `tab`:

    m      → mix help
    m a    → mix archive
    m h    → mix hex
    m a.b  → mix archive.build
    m d.co → mix deps.compile
    m p.n  → mix phoenix.new
