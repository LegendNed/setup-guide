# How to setup a Windows dev environment

Please follow these instructions carefully. If you encounter any roadblocks, contact us on your cohort's Slack channel.

## System requirements

Windows 10 x64 Version 1607 Build 14393 or higher.

## Install Windows Subsystem for Linux

The Windows operating system terminal is different from the UNIX one (used by MacOS and Linux distributions like Ubuntu) and can cause problems with certain workflows we'll use during the course.

Windows 10 has the option to install a subsystem for Linux that effectively lets you work on a Linux evnironment without the need to install a separate operating system.

<details>
<summary>Instructions</summary>

1. Go to **Settings -> Update and Security -> For developers** and turn **Developer mode** on.
2. Go to **Control Panel -> Programs and Features -> Turn Windows features on or off** and turn **Windows Subsystem for Linux** on and click 'OK'.
3. You'll be prompted to restart your computer, click on 'Restart now' to install this new feature.
4. After your computer has restarted, go to the Windows App Store, search for Ubuntu and click on 'Get'.
5. Once finished downloading, go to your start menu and search for 'bash' and hit 'Enter'.
6. This terminal will prompt you to create a UNIX user with a password. **Important:** note thsese down because you'll used them frequently.

For more details, see [this page on Microsoft Developer Network](https://msdn.microsoft.com/en-gb/commandline/wsl/install_guide)

</details>

## Install the Hyper terminal

Hyper is a terminal emulator with more user friendly features than Windows' native terminal. You can download and install it by going to https://hyper.is/

From now on, when I mention "the terminal" I mean Hyper unless specified otherwise.

To access the UNIX terminal just type `bash`.

## Install cURL and Git

cURL is a command line utility that allows you to make requests to websites from the terminal, it comes very handy to run download and install scripts. Don't worry, you won't have to use it that much appart from copy-pasting some commands from instructions. 

Git is the version control system that we'll use to keep track of our code. We'll talk more about it during pre-course and you will use it extensively for the rest of your career as a software developer.

To install them, run the following commands on your terminal:

```
sudo apt-get install curl
sudo apt-get install git
```

## Install Zsh and Oh-My-Zsh

The Z shell and the cosmetic package Oh-My-Zsh allows to have a nicer, clearer looking terminal. One of its main benefits is that it displays colour coded information about your current path, Git branch and status and gives you a ton of handy typing shortcuts for common commands.

<details>
<summary>Instructions</summary>

1. Install ZSH by ruunning the following command on your terminal:

```
sudo apt-get install zsh
```

2. Install `oh-my-zsh` by running the following command on your terminal:

```
curl -L https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh | bash
```

3. By default your terminal will start using bash and you can manually switch to zsh by simply typing `zsh`. We can automate this by following these steps:

  - On your terminal, type `nano ~/.bashrc`. This will open the bash configuration file (`.bashrc`) with the terminal text editor called `nano`.
  - At the beginning of the file add the following line (leave everything else as is):
    ```
    bash -c zsh
    ```
  - To save and exit type `Ctrl+X` then `y` and then hit `Enter`.

4. Currently, Hyper's default shell is Windows' native one, which you are not going to use that often. To make `bash` your default shell, follow these steps:

  - On Hyper, go to **Edit -> Preferences** (or type `Ctrl+,`). This will open a text file on Notepad.
  - On the text file (name `.hyper.js`) look for the part where it says `shell: '',`.
  - Replace that line with the following: `shell: 'C:\\Windows\\System32\\bash.exe',`, save and close the document.
  - When you restart your Hyper terminal it should immediately be using your nice ZSH + oh-my-zsh shell.
  
  Reference: [this tutorial](https://evdokimovm.github.io/windows/zsh/shell/syntax/highlighting/ohmyzsh/hyper/terminal/2017/02/24/how-to-install-zsh-and-oh-my-zsh-on-windows-10.html)

</details>

## Install Node.js

So far you could only run JavaScript code on a web browser, attached to an HTML. Node.js allows us to run JavaScript code directly from our terminal. We'll use Node.js extensively during the course so it's important to have an up-to-date version installed.

<details>
<summary>Instructions</summary>

1. Install `nvm` (Node Version Manager) by running this command:

```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.4/install.sh | bash
```

2. Run `nano ~/.zshrc` and paste the following lines at the beginning of the file. Hit `Ctrl+X`, `y` and `Enter` to save and exit.

```
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh" # This loads nvm
```

3. Restart your terminal.
4. To install the latest stable version of Node.js run this command:

```
nvm install node
```

5. To check the installation was successful run these commands:

```
node -v
npm -v
```

You should see version numbers like `8.4.0` and `5.3.0` or higher respectively.
</details>
