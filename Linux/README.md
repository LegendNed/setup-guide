# How to set up a Linux Dev environment

Copy and paste this command into your terminal.

```bash
sudo apt-get update && sudo apt-get upgrade && sudo apt-get install git && sudo apt-get install terminator curl postgresql postgresql-contrib && touch ~/.bash_profile && curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.6/install.sh | bash && source ~/.nvm/nvm.sh && nvm install node && nvm use node && sudo -u postgres createuser --superuser $USER && sudo -u postgres createdb $USER
```

Then hit return.

This will install the following things:

- [Git](https://git-scm.com/)
- [NVM](https://github.com/nvm-sh/nvm)
- [Terminator](https://gnometerminator.blogspot.com/p/introduction.html)
- [Node](https://nodejs.org/en/)
- [PSQL](https://www.postgresql.org/)

Run this command to enter the terminal application for PostgreSQL:

```bash
psql
```

Now type:

```bash
ALTER USER username WITH PASSWORD 'mysecretword123';
```

BUT Instead of username type your Ubuntu username and instead of 'mysecretword123' choose your own password and be sure to wrap it in quotation marks. Use a simple password like 'password'. DONT USE YOUR LOGIN PASSWORD!

You can exit out of psql by typing \q

And that's it!

If you have any questions or issues then please get in touch on Northcoders-Freshers slack.
