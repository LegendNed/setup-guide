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
4. After your computer has restarted, go to the Microsoft Store, search for Ubuntu and click on 'Get'.
5. Once finished downloading launch Ubuntu. The terminal instance will prompt you to create a UNIX user with a password. **Important:** note thsese down because you'll used them frequently.

For more details, see [this page on Microsoft Developer Network](https://msdn.microsoft.com/en-gb/commandline/wsl/install_guide)

</details>


## Install cURL and Git

cURL is a command line utility that allows you to make requests to websites from the terminal, it comes very handy to run download and install scripts. Don't worry, you won't have to use it that much appart from copy-pasting some commands from instructions. 

Git is the version control system that we'll use to keep track of our code. We'll talk more about it during pre-course and you will use it extensively for the rest of your career as a software developer.

Open Ubuntu and in the terminal instance type:

```
sudo apt-get install curl
sudo apt-get install git
```

## A better terminal application

Change this out for Cmder

Now that we've installed git, we need a better terminal emulator to use it with. Cmder provides us with a lot of the funcitonality we would get on a Unix terminal, and let's us have terminal instances in tabs rather than multiple windows open. The latest version can be downloaded from the link below:

http://cmder.net/

Once Cmder has been installed, open it and type `bash`. You will need to enter this command to run bash whenever you open a new instance of Cmder.

## Install Node.js

So far you could only run JavaScript code on a web browser, attached to an HTML page. Node.js allows us to run JavaScript code directly from our terminal. We'll use Node.js extensively during the course and on the Precourse so it's important to have an up-to-date version installed.

Run this command in your terminal to install Node Version Manager which allows you to easily download the latest version of Node, and switch between versions at a later date if you need to:

`$ curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.6/install.sh | bash`

Check it has installed correctly by typing this command on the terminal:

`$ nvm --version`

Again, if you see a version number you are good.

Now install Node using NVM:

`$ nvm install node`

`$ nvm use node`

You may need to quit and reopen your terminal application before you see it has been successful. To check success, type:

`$ node --version`

If you have an earlier version than 6, type:

`$ nvm install 8.6.0`

`$ nvm use 8.6.0`

`$ node --version` 

Now you should see that you are using Node version 8.6.0


### PostgreSQL

PostgreSQL is another database we'll use during the course. Again, don't worry if this doesn't seem to go as you planned, you won't need it for the Precourse and we can sort you out at the install session!

At the time of writing, the recommended way of installing PostgreSQL on windows is downloading the installer of the official website:

`$ sudo mkdir -p /data/db`

Run the installer and follow the instructions. When asked to provide a password make a note of it and DON'T USE YOUR LOGIN PASSWORD.

once the installation has finished we can run an instance of SQL Shell by launching psql (type 'psql' into the search bar).

Once you've entered your password and logged in, test it's working correctly by typing:

`$ SELECT version();`

And that's it!

If you have any questions or issues then please get in touch on Northcoders-Freshers slack.
