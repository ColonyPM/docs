# values

Copies a package's `values.yaml` file to a specified destination or the current working directory.

## Usage

```bash
cpm pkg values <PKG> [DEST]
```

## Arguments

| Argument | Description | Required |
|----------|-------------|----------|
| `<PKG>` | Name of the package whose values.yaml to copy | Yes |
| `[DEST]` | Destination directory for the copied file | No |

When `[DEST]` is not specified, the file is copied to the current working directory. The copied file will be named `values.<PKG>.yaml`.

## Example

Copy the values.yaml file from the `faas` package to the current directory:

```bash
cpm pkg values faas
```

This creates `values.faas.yaml` in your current directory.

Copy the values.yaml file to a specific directory:

```bash
cpm pkg values faas ./config
```

This creates `values.faas.yaml` in the `./config` directory.

## See Also

- [Package Format](../../Package/format.md) — Full package structure and file reference
