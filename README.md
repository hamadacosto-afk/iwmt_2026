## Installing uv

### Installation methods

Install uv using one of the following methods:

```
# For standalone installer
curl -LsSf https://astral.sh/uv/install.sh | sh

# For PyPI
pip install uv

# For PyPI with isolated environments
pipx install uv

# For Homebrew (macOS)
brew install uv

# For WinGet (Windows)
winget install --id=astral-sh.uv -e
```

## Starting Development

To set up your project for development, use the `uv sync` command:

```
uv sync
```

This command will:

- Create or use a virtual environment for the project.
- Install all dependencies specified in `pyproject.toml` or `uv.lock`.
- Ensure the project is fully prepared for development.

After syncing your project, you can begin development by using the provided commands to run and test your applications. These commands are designed to streamline your workflow and ensure a smooth development experience.

- **Run the API in development mode**:
  ```
  uv run --package api fastapi dev apps/api/main.py
  ```

- **Run the API in production mode**:
  ```
  uv run --package api fastapi run apps/api/main.py
  ```

- **Start all services in development mode**:
  ```
  uv run poe dev
  ```

- **Run a specific app**:
  ```
  uv run poe dev:apps-api
  ```

Follow these steps to ensure your project is properly initialized and ready for development or deployment.












---------
temp:

export ENV_FOR_DYNACONF=production
export IWMT_FIREBASE_JSON_CREDENTIALS="THIS IS SECRET"
