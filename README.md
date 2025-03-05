# Aptos CLI Version Manager - aptosup

This is a simple script to update the Aptos CLI to a specific version.

## Usage

### Install aptosup

You will have to remove your current aptos installation.

Clone the repository.

```bash
git clone https://github.com/LayerZero-Labs/aptosup.git
```

Make the script executable.

```bash
chmod +x aptosup
```

### List installed aptos versions

```bash
sudo aptosup -l
```

### Using Different Aptos Version

```bash
sudo aptosup -v <version>
```

- if you want to install version 3.5.0 for movement network - `sudo aptosup -v 3.5.0`
- if you want to install version 6.0.1 for aptos network - `sudo aptosup -v 6.0.1`

The script checks if the aptos binary already exists in `/usr/local/bin/.aptos` directory. If it does, it will use the existing binary.

If the aptos binary does not exist, it will build from source and install the aptos binary to `/usr/local/bin/.aptos` directory.

### Addition to your .zshrc or .bashrc

```bash
echo "\nexport PATH=\"/usr/local/bin/.aptos:\$PATH\"" >> ~/.zshrc
source ~/.zshrc
```

for bash use `~/.bashrc` instead of `~/.zshrc`
