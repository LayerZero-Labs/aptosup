# Aptos CLI Version Manager - aptosup

This is a simple script to update and install the Aptos CLI to a specific version. It also lets you toggle between different versions of the Aptos CLI.

## Usage

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

### List installed aptos versions

```bash
aptosup -l
```

### Using Different Aptos Version

Note: You might be prompter to enter your sudo password during the process - as it might need to install dependencies via your package manager.

```bash
aptosup -v <version>
```

- if you want to install version 3.5.0 for movement network - `sudo aptosup -v 3.5.0`
- if you want to install version 6.0.1 for aptos network - `sudo aptosup -v 6.0.1`

The script checks if the aptos binary already exists in `/usr/local/bin/.aptos` directory. If it does, it will use the existing binary.

If the aptos binary does not exist, it will build from source and install the aptos binary to `/usr/local/bin/.aptos` directory.

for bash use `~/.bashrc` instead of `~/.zshrc`
