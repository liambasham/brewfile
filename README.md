# Brewfile Setup
This repository stores a Homebrew `Brewfile` so you can recreate this machine setup quickly.

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
