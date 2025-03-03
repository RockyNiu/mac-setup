# Setup a new Macbook 
## common setup for beginner
- Install [chrome](https://www.google.com/chrome/next-steps.html)
- Install xcode 
  - `xcode-select --install`
- Install [brew](https://brew.sh/) 
  - `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
  - remember to follow the instruction shown after brew installation to add `brew` into your path, similar as the following
    ```bash
    echo >> /Users/hong/.bash_profile
    echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/hong/.bash_profile
    eval "$(/opt/homebrew/bin/brew shellenv)"
    ```
- Install [VScode](https://code.visualstudio.com/)
  - Install python plugin
  
### Python Env
- Install [pyenv](https://github.com/pyenv/pyenv) 
  - `brew install pyenv`
  - setup shell environment. For zsh:
    ```bash
    echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
    echo 'command -v pyenv > /dev/null || expot PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
    echo 'eval "$(pyenv init -)"' >> ~/.zshrc
    ```
  - restart shell: `exec $SHELL`
  - install python `pyenv install 3.11` (choose a version you like)
- Install [poetry](https://github.com/python-poetry/poetry) 
  - `curl -sSL https://install.python-poetry.org | python - --version 1.8.3` (recommend) or `brew install poetry`(for 2.0+)
  - setup shell environment. For zsh:
  ```bash
  echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.zshrc
  ```
  - restart shell: `exec $SHELL`
- Install [Github Desktop](https://desktop.github.com/download/)
  - Sign in with your github account 
- Env setting:
  - in the folder, `poetry env use 3.11` and `poetry init`
  - in VScode, `Shift + Cmd + P` => `Python: Select Interpreter` => Select `Python 3.11***** : Poetry` as your virtual environment
  - Add dependencies
    - If there is `pyproject.toml`, `poetry install`
    - Otherwise, add the denpendencies as `poetry add pandas@2.2.0`
      
### Ruby Env
- Install [rbenv](https://github.com/rbenv/rbenv)
  -  `brew install rbenv ruby-build`
  -  `rbenv init`
- Install ruby
  - `rbenv install 3.3.7`
  - `rbenv global 3.3.7`

