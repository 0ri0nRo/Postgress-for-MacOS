# Postgress guide for MacOS


## Requirements
> **Install Brew**
> You need to install `brew` with this command:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

> **Install Postgres.app**
> Go on (Postgres.app)[https://postgresapp.com/] and install it on "Downloads" session. 


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

After open PostgreSQL, if you  write and run `psql` on your terminal you should see:

```bash
your_name\=\#
```

Now we install `pgweb` with this command:
```bash
brew install pgweb
```


```bash
cd openmodelica-apple-silicon
chmod +x install.sh
./install.sh
```