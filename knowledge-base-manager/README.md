# KBM (Knowledge Base Manager)

**KBM** is a lightweight script designed to handle the creation and renaming of files in a structured Knowledge Base.
It enforces a consistent naming convention and integrates with Orbix.

## Features

- **Create new files** with a consistent naming convention:
  `<YYYY-MM-DD>_<type>_<title>.<extension>`
  
- **Rename existing files** to match the same convention.

- **Targeted directories**: Save files automatically in `Projects`, `Areas`, `Archives`, or `Resources` directories using flags.

- **Flexible file types**: Specify file types like `note`, `script`, or `document`.

## Naming Convention

- **Date**: Automatically prepended using the current date or file's last modified date.
- **Type**: Indicates the category (e.g., `note`, `script`, `doc`).
- **Title**: Concise description in lowercase, with spaces replaced by hyphens.

### Examples

1. Creating a new note:
   ```
   2025-01-10_note_pqc-research.md
   ```
2. Renaming a script:
   ```
   2025-01-05_script_switch-theme.sh
   ```

## Usage

### Commands

1. **Create a new file**:
   ```bash
   kbm new -[type] -[directory] <title> <extension>
   ```
   - **Flags**:
     - `-n`: Note
     - `-s`: Script
     - `-d`: Document
     - `-P`: Save to `Projects`
     - `-A`: Save to `Areas`
     - `-Arc`: Save to `Archives`
     - `-R`: Save to `Resources`
   - **Example**:
     ```bash
     kbm new -n -P research-summary md
     ```

2. **Rename an existing file**:
   ```bash
   kbm rename -[type] -[directory] <old_filepath> <new_title>
   ```
   - **Flags**:
     - Same as for the `new` command.
   - **Example**:
     ```bash
     kbm rename -s -R ~/old-script.sh theme-updater
     ```

## Installation

1. Save the `kbm` script in a directory in your PATH (e.g., `~/bin`).
2. Make it executable:
   ```bash
   chmod +x ~/bin/kbm
   ```

## Notes

- KBM is designed as part of the Orbix workflow and assumes directories like `Projects`, `Areas`, `Archives`, and `Resources` exist under `~/Workspace/KnowledgeBase`.
- For additional flexibility, modify the script to fit your specific needs.

---
