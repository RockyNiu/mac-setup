# Setup a new Macbook
- Install [chrome](https://www.google.com/chrome/next-steps.html)
- Install xcode `xcode-select --install`
- Install [brew](https://brew.sh/) `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
  - remember to follow the instruction shown after brew installation to add `brew` into your path
- Install pyenv `brew install pyenv`
  - setup shell enironment. For zsh:
    ```bash
    echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
    echo 'command -v pyenv > /dev/null || expot PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
    echo 'eval "$(pyenv init -)"' >> ~/.zshrc
    ```
  - restart shell: `exec $SHELL`
