To use `uv` for managing dependencies in your project, follow the instructions below. This guide is designed to save you the trouble of reading the full documentation, but if you'd like more details, feel free to visit: https://docs.astral.sh/uv/guides/projects/

### Adding a Package
To add a package, you can specify the version explicitly or let `uv` fetch the latest version:
```
uv add 'requests==2.31.0'
```
or
```
uv add requests
```

### Adding Packages from a Requirements File
To add packages listed in a `requirements.txt` file, along with an optional constraints file, run:
```
uv add -r requirements.txt -c constraints.txt
```

### Adding a Package to an App's Dependencies
To add a package to the dependencies of a specific app, use the `--workspace` flag. For example:
```
uv add --package api constants agromath --workspace
```

### Installing Dependencies in a Specific Package
To install dependencies for a specific package, specify the package name and the dependency. For example:
```
uv add --package api "fastapi[standard]"
```

### Upgrading a Package
To upgrade a specific package (e.g., `requests`), run:
```
uv lock --upgrade-package requests
```

### Removing a Package
To remove a package, use:
```
uv remove requests
```

To sync all packages and groups after installs and changes, run:
```
uv sync --all-packages --all-groups
```
