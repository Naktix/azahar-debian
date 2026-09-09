# Azahar for Debian

Unofficial APT repository for [Azahar](https://github.com/azahar-emu/azahar).

This repository builds Azahar as a native `.deb` package for **Debian 13 (Trixie)** and publishes the package through a signed APT repository hosted on GitHub Pages.

## How to install

Add the repository signing key and apt repository:

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

Remove the apt repository and repository signing key:

```bash
sudo rm /etc/apt/sources.list.d/azahar.list

sudo rm /etc/apt/keyrings/azahar.gpg
```

Update the package lists:

```bash
sudo apt update
```
