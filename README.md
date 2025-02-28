# Setup a new Macbook
- Install [chrome](https://www.google.com/chrome/next-steps.html)
- Install xcode `xcode-select --install`
- Install [brew](https://brew.sh/) `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
  - remember to follow the instruction shown after brew installation to add `brew` into your path
- Install [pyenv](https://github.com/pyenv/pyenv) `brew install pyenv`
  - setup shell environment. For zsh:
    ```bash
    echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
    echo 'command -v pyenv > /dev/null || expot PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
    echo 'eval "$(pyenv init -)"' >> ~/.zshrc
    ```
  - restart shell: `exec $SHELL`
  - install python `pyenv install 3.11` (choose a version you like)
- Install [poetry](https://github.com/python-poetry/poetry) `brew install poetry`(for 2.0+) or `curl -sSL https://install.python-poetry.org | python - --version 1.8.3`
  - setup shell environment. For zsh:
  ```bash
  echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.zshrc
  ```
  - restart shell: `exec $SHELL`
