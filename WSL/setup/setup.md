# How to setup up your WSL dev environment

First things first here's a little tip that with dramatically improve your experience when using the command line.

- Open up Ubuntu from the start menu if you haven't already got it open, right click on the top bar and select properties. In the properties you can check the box which will enable you to use `CTRL-C` and `CTRL-V` shortcuts on the command line.

Now the above is done this next step will be much easier.

Next please copy and paste the following into your terminal:

```bash
sudo apt-get update && sudo apt-get upgrade && sudo apt-get install git && touch ~/.bash_profile && curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash && source ~/.nvm/nvm.sh && nvm install node && nvm use node &&  git config --global credential.helper store
```

Then hit return.

This will install the following things:

- [Git](https://git-scm.com/)
- [NVM](https://github.com/nvm-sh/nvm)
- [Node](https://nodejs.org/en/)

---

Next step lets install Postgres.

Please copy and paste the following into your terminal:

```bash
sudo apt install postgresql postgresql-contrib
```

Then hit return again, this will install [PSQL](https://www.postgresql.org/).

A few more steps and we're done!

1. Enter the command: `sudo passwd postgres`
2. You will get a prompt to enter your new password
3. Close and reopen your terminal.

Finally paste this command into your terminal `sudo service postgresql start && sudo -u postgres psql` and you should see something like the following:

```bash
postgres=#
```

You can exit Postgres by typing `\q` and hitting return.

And that's everything you need to get started!