# File Cleaner (fcl):

## Overview
The `fcl` script automates the process of organizing files. It allows you to:
- Select a category and location for files.
- Rename files based on a standardized naming convention (e.g., hyphenated lowercase titles).
- Move files to a structured directory (e.g., KnowledgeBase Resources, Projects, etc.).

This script uses `kbm` internally to handle renaming and moving tasks.

## Commands

### Process a Directory
The script processes all files in a specified directory (default: `~/Downloads`):
```bash
fcl [directory]
```
- If no directory is specified, it defaults to `~/Downloads`.
- Prompts for category, location, and a new title for each file.

### Features
1. **Category Selection**:
   - Choose a category for the file (e.g., `note`, `script`, `doc`, `image`, `misc`).
2. **Location Selection**:
   - Choose a destination directory (e.g., `Resources`, `Projects`, `Archives`).
3. **Title Linting**:
   - Ensures the file name follows a standard format:
     - Replaces spaces with hyphens.
     - Removes invalid characters.
     - Converts the title to lowercase.

### Example Usage
1. Run the script for the `~/Downloads` directory:
```bash
fcl ~/Downloads
```
2. For each file, you'll:
   - Decide whether to process it.
   - Select a category from a menu (e.g., `note`, `doc`).
   - Select a location (e.g., `Resources`, `Archives`).
   - Provide a new, sanitized title (e.g., `project-summary`).
3. Files will be renamed and moved accordingly.

## Integration with `kbm`
The script relies on the following `kbm` commands:

### Rename an Existing File
```bash
kbm rename -[type] -[directory] <old_filepath> <new_title>
```
- **Flags**:
  - `-n`: Note
  - `-s`: Script
  - `-d`: Document
  - `-R`: Resources
  - `-D`: Documents
  - `-I`: Pictures
  - `-P`: Projects
  - `-Arc`: Archives
  - `-A`: Areas

### Example:
```bash
kbm rename -n -R ~/old-file.md project-summary
```
Renames `old-file.md` to `project-summary.md` in the `Resources` directory.

## Notes
- Ensure `kbm` is installed and configured before using `fcl`.
- The script skips any file you choose not to process.
- Categories and locations are predefined but can be expanded in the script if needed.

## Troubleshooting
If a file isn't processed correctly:
1. Check the `kbm` command being run (logged during execution).
2. Ensure the selected category and location are valid.
3. Verify directory permissions for the target location.

