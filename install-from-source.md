# Install from source

You will have to remove your current aptos installation.

If you have a previous installation - run the following command.

```bash
$ whoami
<USER>
```

```bash
$ ls -la ~/.aptosup 
total 16
-rwxr-xr-x   1 <USER>     staff  4780  9 Mar 10:56 aptosup
drwxr-xr-x   2 <USER>     staff    64  9 Mar 10:56 tmp
```

at `$USER` if you see your login name you're good. If it is `root` you'll have to run the following command.

```bash
sudo chown -R $USER: ~/.aptosup
```

This will change the ownership of the `~/.aptosup` directory to your user.

### Clone the repository

```bash
git clone https://github.com/LayerZero-Labs/aptosup.git
```

### Install aptosup - this can also be used to update aptosup

```bash
chmod +x install
```

```bash
./install
```
