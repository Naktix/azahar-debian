# Azahar for Debian

This repository builds [Azahar](https://github.com/azahar-emu/azahar) as a native .deb package and publishes it on GitHub Pages.

## How to install

Add the signing key and repository:

```bash
curl -fsSL https://naktix.github.io/azahar-debian/azahar.gpg | sudo tee /etc/apt/keyrings/azahar.gpg > /dev/null

echo "deb [arch=amd64 signed-by=/etc/apt/keyrings/azahar.gpg] https://naktix.github.io/azahar-debian trixie main" | sudo tee /etc/apt/sources.list.d/azahar.list
```

Update the package lists:

```bash
sudo apt update
```

Install Azahar:

```bash
sudo apt install azahar
```

## How to remove

Remove Azahar:

```bash
sudo apt remove azahar
```

Remove the repository and signing key:

```bash
sudo rm /etc/apt/sources.list.d/azahar.list

sudo rm /etc/apt/keyrings/azahar.gpg
```

Update the package lists:

```bash
sudo apt update
```

> **Disclaimer:** This is an unofficial repository and is not affiliated with, endorsed by, or officially supported by the Azahar Emulator Project.
