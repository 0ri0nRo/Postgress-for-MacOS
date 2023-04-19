# Postgress guide for MacOS
# Contents

- [Requirements](##Requirements)
- [Install Brew](###InstallBrew)
- [Postgres.app](#curriculum)
- [Install Pgweb](#code-of-conduct)
- [On terminal](#team)
- [Open & Use](#team)
- [Common errors](#team)

## Requirements

### Install Brew

You need to install `brew` with this command:

  

```bash

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

```

### Postgres.app

Go on [Postgres.app](https://postgresapp.com/) and install it on "Downloads" session.

  

### Install Pgweb

Now we install `pgweb` with this command:

```bash

brew install pgweb

```

  

## On terminal

  

Now open your terminal and check your $SHELL. You can check with this command:

```bash

echo $0

```

If your $SHELL is "zsh" copy this command:

```bash

echo 'export PATH=/Applications/Postgres.app/Contents/Versions/15/bin:$PATH' >> ~/.zshrc

```

  

If your $SHELL is "bash" copy this command:

  

```bash

echo 'export PATH=/Applications/Postgres.app/Contents/Versions/15/bin:$PATH' >> ~/.bashrc

```

## Open & Use

After open PostgreSQL, if you write and run `psql` on your terminal you should see:

```bash

your_name\=\#

```

  

To conclude open `pgweb`:

```bash

pgweb

```

  

## Common errors

### PostgreSQL - port 5432 already in use

To check what is running on port 5432, issue the following command on your terminal.

```bash

sudo lsof -i :5432

```

  

My output:

```bash

COMMAND PID USER FD TYPE DEVICE SIZE/OFF NODE NAME

postgres 482 postgres 7u IPv6 0xe7f8dbd595be4cbd 0t0 TCP *:postgresql (LISTEN)

postgres 482 postgres 8u IPv4 0xe7f8dbd5962f87d5 0t0 TCP *:postgresql (LISTEN)

```

  

Now kill all PostgreSQL `postgres` processes, issue the following command.

```bash

sudo pkill -u postgres

````

### Note

If your output is different then you will have to kill those processes of that program.