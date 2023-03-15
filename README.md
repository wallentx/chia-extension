# Chia-Extension
### A Package Manager for Chia

`chia-extension` is a package manager designed specifically for Chia, making it easy to discover, install, and manage extensions for your Chia farming experience.

## Features

- Discover* and install extensions from various repositories.
- Manage installed extensions in a centralized manner.
- Automatically build and link extension artifacts to your Chia virtual environment.

## Installation

1. Add `chia-extension` to your `PATH`.
2. `cd` to your `chia-blockchain` repo.
3. Run `chia-extension`.

## Usage

To install an extension, run:

```bash
chia-extension -i <extension-repo-url> <branch (optional- will use default branch if none specified)>
```
For example:

```bash
chia-extension -i https://github.com/wallentx/almanac
```
This command clones the extension repository and prompts you to confirm the execution of required build commands. After confirmation, chia-extension builds the extension, links the artifacts to your Chia virtual environment, and installs the extension.

## Output
An example output when installing an extension:

```bash
📥 Cloning extension...✓
⚠️ The following commands will be executed within '$HOME/chia-blockchain/ext/extension-name':
source ../../activate && pip install some-package

Do you want to run these commands? [Y/n]
🏗️ Building... ✓
🔗 Linking artifacts...✓
🏁 Done!
📦 The following artifacts have been symlinked to your venv:
almanac
🧩 'almanac' has been installed.
```
