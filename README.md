# Aptos CLI Version Manager - aptosup

This is a simple script to update and install the Aptos CLI to a specific version. It also lets you toggle between different versions of the Aptos CLI.

## Usage

### Prerequisite - install dependencies if required 

If you run into issues related to dependencies or you get a false positive install successful message please refer - <https://aptos.dev/en/network/nodes/building-from-source#set-up-build-dependencies> for a list of dependencies that aptos requires.

### Install aptosup

```bash
curl -sSL https://raw.githubusercontent.com/LayerZero-Labs/aptosup/main/install | bash
```

### Install aptosup from source

For installing from source please refer to [Install from source](install-from-source.md)

### Addition to your .zshrc or .bashrc

```bash
echo "export PATH=\"$HOME/.aptosup:\$PATH\"" >> ~/.zshrc
```

and then refresh your shell

```bash
source ~/.zshrc
```

for bash use `~/.bashrc` instead of `~/.zshrc`

### List installed aptos versions

```bash
aptosup -l
```

### Installing aptos version

Note: You will be prompted to enter your sudo password during the process - as it might need to install dependencies via your package manager.

#### Install and set as active version

This sets the default version to be installed and set as active version.

```bash
aptosup -d <version>
```

#### Only install

```bash
aptosup -i <version>
```

This only installs the new version, you will need to set it as active version manually.

- if you want to install version 3.5.0 for movement network - `aptosup -i 3.5.0`
- if you want to install version 6.0.1 for aptos network - `aptosup -i 6.0.1`

The script checks if the aptos binary already exists in `$HOME/.aptos`. If it does, it switches the current active version to the new installed version.

### Set active installed aptos version

```bash
aptosup -s <version>
```

### Remove installed aptos version

```bash
aptosup -r <version>
```

### Update aptosup

```bash
aptosup -u
```
