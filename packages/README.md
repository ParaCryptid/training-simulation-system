# Offline Python Packages

This directory contains all required `.whl` (wheel) files for offline installation.

To generate:
```bash
pip download -r requirements.txt --dest packages/
```

To install:
```bash
pip install --no-index --find-links=packages -r requirements.txt
```
