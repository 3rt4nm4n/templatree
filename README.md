# Templatree

**Templatree** is a lightweight Python CLI tool that scaffolds directory structures from simple text templates, flat paths or file lists. It also supports automatic virtual environment creation.

## Features

- Generate project folders from:
  - A tree-style structure (e.g., `├── main.py`)
  - A flat path list (`project/static/index.html`)
- Load structure from an external `.txt` file using `--from-file`
- Create a virtual environment inside the project with `-venv`
- Clean and simple CLI interface

---

## Example use cases:

### Template:

```bash
templatree create exampleproject
Would you like to send a (1) tree-style template or (2) flat path list? (1 or 2): 1
Enter your structure (end with a line containing only 'EOD'):
exampleproject/
├── main.py
├── static/
│   ├── index.html
│   ├── index.css
│   └── index.js
├── config/
│   └── settings.py
├── requirements.txt
└── README.md
EOD
```

### Flat paths:

```bash
templatree create myproj
Would you like to send a (1) tree-style template or (2) flat path list? (1 or 2): 2
Enter your structure (end with a line containing only 'EOD'):
myproj/main.py
myproj/static/index.html
myproj/static/index.css
myproj/static/index.js
myproj/config/settings.py
myproj/requirements.txt
myproj/README.md
EOD
```

### From a file:

```bash
templatree create -venv example_virtualenv --from-file example.txt exampleproject
```

## Installation

```bash
pip install templatree
```

---
