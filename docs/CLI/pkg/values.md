# values

Copies a package's `values.yaml` file to a specified destination or the current working directory.

## Usage

```bash
cpm pkg values <PKG> [DEST]
```

## Arguments

| Argument | Description                                   | Required |
| -------- | --------------------------------------------- | -------- |
| `<PKG>`  | Name of the package whose values.yaml to copy | Yes      |
| `[DEST]` | Destination **path** (directory or filename)  | No       |

- If `[DEST]` is a **directory** (or omitted), the file is saved as `values.<PKG>.yaml`.
- If `[DEST]` is a **file path**, the file is saved with that specific name.

> **Note:** This command will **not** overwrite existing files.

## Examples

**Default Usage:**
Copy the values.yaml file from the `faas` package to the current directory:

```bash
cpm pkg values fibbers
# Creates: ./values.fibbers.yaml
```

**Copy to a Directory:**
Copy the file into a specific folder:

```bash
cpm pkg values fibbers ./config
# Creates: ./config/values.fibbers.yaml
```

**Rename the File:**
Copy the file with a custom name:

```bash
cpm pkg values fibbers ./my-custom-config.yaml
# Creates: ./my-custom-config.yaml
```

## See Also

- [Package Format](../../Package/format.md) — Full package structure and file reference
