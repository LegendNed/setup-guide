# How to setup an macOS dev environment

## New Mac Setup for Apple Silicon M1 Chips ONLY - (Ignore if your Mac has an Intel chip)

### Rosetta terminal

1. Duplicate the `Terminal` app (or iTerm, if that is the terminal you are going to use) and rename it. Then, open `Finder` and navigate to the `Application/Utilities` folder and select "Duplicate." 
2. Rename this new terminal to something like "Terminal-Rosetta" Now right-click on your new Rosetta Terminal and click "Get info." 
3. From the “Get info” menu, select "Open using Rosetta."

_Now we have a special terminal that can be used to install our command line tools. During the install, they will be translated by Rosetta. After the install, we can use them from the native terminal._

References: 
- [Set up an M1 MacBook for web development blog](https://blog.logrocket.com/set-up-macbook-for-web-development-in-20-minutes/)
- [Tips and Tricks to Set Up Your Apple M1 for Development](https://www.courier.com/blog/tips-and-tricks-to-setup-your-apple-m1-for-development/)

## Intel & Apple Silicon M1

Copy and paste this command into your terminal (the Rosetta terminal if you have Apple Silicon M1).

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)" && curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash && source ~/.nvm/nvm.sh && nvm install node && nvm use node && brew install postgresql && brew install zsh zsh-completions && sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

Then hit return.

This will install the following things:

- [Brew](https://brew.sh/)
- [Node](https://nodejs.org/en/) via [NVM](https://github.com/nvm-sh/nvm#install--update-script)
- [PSQL](https://www.postgresql.org/)
- [zsh](https://www.zsh.org/)
- [oh-my-zsh](https://ohmyz.sh/)
