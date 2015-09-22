Mix completion plus shortcuts and colors
========================================

Bash autocompletion for Elixir [mix](http://elixir-lang.org/getting-started/mix-otp/introduction-to-mix.html).

## Power features

### Shortcuts

You can invoke tasks in a shorter way without pressing `TAB`:

    m      → mix help
    m a    → mix archive
    m h    → mix hex
    m a.b  → mix archive.build
    m d.co → mix deps.compile
    m p.n  → mix phoenix.new

### Colors

When you execute `m` (or `m help`), tasks are colored green.

## Install via homebrew

`brew tap homebrew/completions`

`brew install mix-completion`

More about [homebrew completions](https://github.com/Homebrew/homebrew-completions).

## Manual install

Global:

    $ git clone git@github.com:davidhq/mix-power-completion.git
    $ cd mix-power-completion
    $ sudo cp mix /etc/bash_completion.d/
    $ source /etc/bash_completion.d/mix
    (on new terminal tabs, this should be autoloaded)

Local:

    $ ~/bash_completion.d
    $ cp mix ~/bash_completion.d/

Add to `~/.bashrc`:

    if [ -f "$HOME/bash_completion.d/mix" ] ; then
        source $HOME/bash_completion.d/mix
    fi

## Usage

To list all currently avaliable mix tasks:

    $ m [TAB]
      archive            archive.uninstall        ....

    $ mix [TAB]
      archive            archive.uninstall        ....

To complete command:

    $ m t[TAB]
      m test

There will be a slight lag because mix has to check what is available for the current project.
