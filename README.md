# Backup File Finder for Bug Bounty

This Python script is designed for bug bounty hunters and security researchers to find backup files on web servers. The script scans target domains for potential backup file URLs based on common file extensions (e.g., `.zip`, `.rar`, `.sql`) and a custom wordlist. It verifies if the files are valid downloadable backups.

## Features

- Scans a single target domain or multiple domains (provided in a file).
- Searches for backup files with common extensions (e.g., `.zip`, `.sql`, `.tar`).
- Uses a custom wordlist to generate potential file names.
- Checks for valid downloadable backup files by inspecting HTTP responses.
- Saves valid backup file links to a timestamped file for later analysis.

## Requirements

Before using the script, make sure you have Python 3.x installed. The script requires the following Python libraries:

- `requests`
- `colorama`
- `tqdm`

You can install the required dependencies by running:

```bash
pip install -r requirements.txt
```
## Usage
```bash
python ex-backup.py  -l domains.txt  -w backup-wordlist.txt
