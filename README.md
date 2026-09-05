# Christopherstaton Tap

## How do I install these formulae?

`brew install christopherstaton/tap/<formula>`

Or `brew tap christopherstaton/tap` and then `brew install <formula>`.

Or, in a `brew bundle` `Brewfile`:

```ruby
tap "christopherstaton/tap"
brew "<formula>"
```

## Windows (no Homebrew)

Homebrew doesn't run natively on Windows. `claude-swap` is a Python CLI, so the
equivalent one-command install is [pipx](https://pipx.pypa.io) (isolated app
install, just like a Homebrew formula):

```bash
python -m pip install --user pipx
python -m pipx ensurepath
pipx install "git+https://github.com/christopherstaton/claude-swap.git@v0.27.0b1-fork4"
```

This installs the `cswap` / `claude-swap` commands. Requires Python 3.12+.

- Upgrade: `pipx upgrade claude-swap`
- Latest fork main: `pipx install "git+https://github.com/christopherstaton/claude-swap.git@main"`
- Uninstall: `pipx uninstall claude-swap`

The macOS menu bar (`cswap menubar`, via `rumps`/`pyobjc`) is macOS-only and
prints a clear "only available on macOS" message there. Verified working on
Windows: `status`, `config`, `statusline`, `alias`, and `map`. The Textual TUI
(`cswap tui`) and account switching are cross-platform but exercise best in an
interactive terminal.

## Documentation

`brew help`, `man brew` or check [Homebrew's documentation](https://docs.brew.sh).
