# Init Command

Initialize a new package with the standard directory structure and required files.

## Usage

```bash
cpm pkg init [path]
```

## Arguments

| Argument | Description | Required |
|----------|-------------|----------|
| `[path]` | Directory to initialize the package in | No (defaults to current directory) |

## What It Does

1. Creates the package directory (if a path is provided)
2. Creates a `templates/` subdirectory
3. Generates a `package.yaml` [manifest](https://docs.colonypm.xyz/Package/manifest) with default values
4. Creates a `values.yaml` file with a `global:` section
5. Creates a `README.md` 

## Generated Structure

```text
<package-name>/
├─ package.yaml
├─ README.md
├─ templates/
└─ values.yaml
```

## Examples

Initialize a package in the current directory:

```bash
cpm pkg init
```

Initialize a new package in a specific directory:

```bash
cpm pkg init /path/to/package
```


## See Also

- [Package Format](https://docs.colonypm.xyz/Package/format) — Full package structure and file reference
- [Package Manifest](https://docs.colonypm.xyz/Package/manifest) — Detailed information about the package manifest file
