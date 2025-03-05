# Aptos CLI Version Manager - aptosup

This is a simple script to update the Aptos CLI to a specific version.

## Usage

### Install aptosup

You will have to remove your current aptos installation.

Clone the repository.

```bash
git clone https://github.com/LayerZero-Labs/aptosup.git
```

Install aptosup - this can also be used to update aptosup

```bash
chmod +x install.sh
```

```bash
sudo ./install.sh
```

### Addition to your .zshrc or .bashrc

```bash
echo "export PATH=\"$HOME/.aptosup:\$PATH\"" >> ~/.zshrc
source ~/.zshrc
```

### List installed aptos versions

```bash
sudo aptosup -l
```

### Using Different Aptos Version

Note: You might be prompter to enter your sudo password during the process - as it might need to install dependencies via your package manager.

```bash
sudo aptosup -v <version>
```

- if you want to install version 3.5.0 for movement network - `sudo aptosup -v 3.5.0`
- if you want to install version 6.0.1 for aptos network - `sudo aptosup -v 6.0.1`

The script checks if the aptos binary already exists in `/usr/local/bin/.aptos` directory. If it does, it will use the existing binary.

If the aptos binary does not exist, it will build from source and install the aptos binary to `/usr/local/bin/.aptos` directory.



for bash use `~/.bashrc` instead of `~/.zshrc`
