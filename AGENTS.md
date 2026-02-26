# AGENTS.md

## Cursor Cloud specific instructions

### Repository Overview

This is a **distribution/metadata-only repository** for **DiffReader**, a Windows desktop diff viewer application. The repository does **not** contain source code — it serves as a release metadata hub.

### Repository Contents

- `README.md` — Project description and feature list
- `version.json` — Version metadata (version number, release date, download URLs, changelog) pointing to pre-built `.exe` binaries on GitHub Releases
- `LICENSE` — MIT License

### Important Notes

- **No source code**: The actual application source (likely C#/.NET WPF/WinForms) is maintained elsewhere. This repo only hosts release metadata.
- **No build system**: There is no `package.json`, `.csproj`, `Makefile`, `Dockerfile`, or any build configuration.
- **No dependencies to install**: No package manager is used.
- **No tests, linting, or CI**: None are configured in this repository.
- **No dev server**: There is nothing to run locally beyond validating JSON structure.

### What You Can Do

- Validate `version.json` is well-formed JSON: `python3 -c "import json; json.load(open('version.json')); print('OK')"`
- Edit `README.md` for documentation updates
- Update `version.json` when new releases are published
- Verify release URLs are accessible: `curl -sI "<downloadUrl>/<file>"`
