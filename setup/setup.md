# How to setup up your WSL dev environment

First things first here's a little tip that with dramatically improve your experience when using the command line.

## 1. Open your Ubuntu terminal

Open up **Ubuntu** from the start menu if you haven't already got it open - **This is the only terminal that you should be using from now on**

Then right click on the top bar and select _properties_. In the properties you can check the box which will enable you to use `CTRL-C` and `CTRL-V` shortcuts on the command line.

Now the above is done this next step will be much easier.

## 2. Install Git, NVM & Node

Please copy and paste the following into your terminal:

```bash
sudo apt-get update && sudo apt-get upgrade && sudo apt-get install git && curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash && source ~/.nvm/nvm.sh && nvm install node && nvm use node &&  git config --global credential.helper store
```

Then hit return.

This will install the following things:

- [Git](https://git-scm.com/)
- [NVM](https://github.com/nvm-sh/nvm)
- [Node](https://nodejs.org/en/)

---

## 3. Install Postgres.

Please copy and paste the following into your terminal:

```bash
sudo apt install postgresql postgresql-contrib
```

Then hit return again, this will install [PSQL](https://www.postgresql.org/).

A few more steps and we're done!

1. Enter the command: `sudo passwd postgres`
2. You will get a prompt to create a new password for postgres - this is different to your Windows login. After this please close and re-open your terminal.
3. One more command to run in the terminal: `sudo -u postgres createuser --superuser $USER && sudo -u postgres createdb $USER`. You will likely be asked for the password that you just created.


> If you see the following error: `Could not connect to server/database...` or similar, run the following command to ensure that the postgresql server is running before trying the above again:
>
> ```bash
> sudo service postgresql start
> ```

Finally enter `psql` in your terminal and you should see something like this:

```bash
YOUR_USERNAME_HERE=#
```

You can exit Postgres by typing `\q` and hitting return.

And that's everything you need to get started!

---

**Going forward please only use the Ubuntu terminal or the integrated WSL terminal in VSCode**

If you want to use the integrated terminal in VSCode make sure it's the right kind. It is likely that it might assume you want to use PowerShell - _**you shouldn't need to use PowerShell at all**_.

You can switch to Ubuntu/WSL by selecting the drop down arrow next to the plus sign and choosing **Ubuntu(WSL)**:

![Image of PowerShell integrated terminal](/images/integrated-terminal.png 'How to switch to switch to the WSL integrated terminal')

After doing this your terminal should now look something like this:

![Image of WSL integrated terminal](/images/integrated-terminal-wsl.png 'This is what your terminal should look like in VSCode')
