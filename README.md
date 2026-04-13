# Brewfile Setup
This repository stores a Homebrew `Brewfile` so you can recreate this machine setup quickly.

## Fresh machine setup (nothing installed)
Run this single command in Terminal:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)" && \
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile && \
eval "$(/opt/homebrew/bin/brew shellenv)" && \
curl -fsSL https://raw.githubusercontent.com/liambasham/brewfile-repo/main/Brewfile -o ~/Brewfile && \
brew bundle --file=~/Brewfile
```
> **Note:** This assumes Apple Silicon (M1/M2/M3). For Intel Macs, replace `/opt/homebrew` with `/usr/local`.


## Prerequisites
- Install Homebrew first: https://brew.sh

## Restore this environment
From this repository directory, run:

```bash
brew bundle --file=Brewfile
```

This installs all formulas and casks listed in `Brewfile`.

## Verify installed packages
Run:

```bash
brew bundle check --file=Brewfile
```

If everything is installed, Homebrew reports success without making changes.

## Update the Brewfile after environment changes
After installing/removing apps or formulas, regenerate the file:

```bash
brew bundle dump --force
```

Then review and commit the updated `Brewfile`.
