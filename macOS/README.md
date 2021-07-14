# How to setup an macOS dev environment

Copy and paste this command into your terminal.

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)" && curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash && source ~/.nvm/nvm.sh && nvm install node && nvm use node && brew install postgresql && brew install zsh zsh-completions && sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

Then hit return.

This will install the following things:

- [Brew](https://brew.sh/)
- [Node](https://nodejs.org/en/) via [NVM](https://github.com/nvm-sh/nvm#install--update-script)
- [PSQL](https://www.postgresql.org/)
- [zsh](https://www.zsh.org/)
- [oh-my-zsh](https://ohmyz.sh/)
