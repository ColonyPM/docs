# init

Initialize a new package with the standard directory structure and required files.

## Usage

```bash
cpm pkg init [DEST]
```

## Arguments

| Argument | Description | Required |
|----------|-------------|----------|
| `[DEST]` | Directory to initialize the package in | No |

When `[DEST]` is not provided, the package will be initialized in the current directory. The package name will be derived from the directory name.

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

- [Package Format](../../Package/format.md) — Full package structure and file reference
- [Package Manifest](../../Package/manifest.md) — Detailed information about the package manifest file
