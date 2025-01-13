# Orbix

Orbix is a flexible and efficient workflow standard designed to help you organize your digital life.
Whether you're managing projects, taking notes, or automating your setup, Orbix provides a clear and extensible structure to simplify your workflow. 
Perfect for students, professionals, and hobbyists alike, Orbix makes it easy to stay focused, productive and manage backups.

### Filename convention

```
<YYYY-MM-DD>_<type>_<title-or-purpose>.<extension>
```
- **Date:** Helps sort out file chronologically and track changes.
- **Type:** Indicate file's category (e.g., notes, research, script, doc, report, etc.).
- **Title or purpose:** A concise description, using lowercase and hyphens for spaces.

#### Examples

- 2025-01-10_notes_pqc-research.md
- 2025-01-05_script_switch-theme.sh
- 2025-01-03_doc_linux-guide.pdf


### Directory tree

Orbix organizes your workspace into distinct directories to maintain clarity and efficiency. Below is the structure and an explanation of each part:

#### Core file tree
```
~/Workspace/
├── Archives/           # Completed or inactive projects and files
├── Configs/            # System and application configuration files
├── KnowledgeBase/      # Notes, research and references (second brain)
└── Projects/           # Active projects
```

#### Archives
```
~/Workspace/Archives/
```
- Stores completed or inactive projects and files.
- Use this to declutter active directories while retaining past work for reference.

#### Configs
```
~/Workspace/Configs/
├── Ansible/
├── Dotfiles/
```
- **Ansible:** Playbooks and automation scripts.
- **Dotfiles:** Configuration files. These should be symlinks to files in ```~/config/``` for easy management.

#### KnowledgeBase
```
~/Workspace/KnowledgeBase/
```
- Central repository for notes, research and references.
- You can organize this directory using your preferred method (e.g., PARA, Zettelkasten, etc.).















