# Remove

Removes packages in the standard directory. 
## Usage

```bash
cpm pkg remove <package-name[@version]> [--all]
```

 
## Arguments

| Argument | Description | Required |
|----------|-------------|----------|
| `<package-name>` | Path to the package | Yes |
|[@version] | Version number | No |

**Note:**  The function searches for the package version after the delimiter "@". If not found, it will by default assume removal of the entire package.  

## Flags  

| Flag | Description | Required |
|------|-------------|----------|
| `--all` | Confirmation to delete all versions of the package. | No |
 
 **Note:** *--all* can be viewed as a prevantative measure to stop unintended removal.


## Examples

**Remove version:**
Remove package version 1.2.3
```bash
cpm pkg remove testpackage@1.2.3
```

**Remove package:** Removes the parent folder and its contained versions.
```bash
cpm pkg remove testpackage --all
#Output:
package testpackage removed
```

## See Also

- [Package Format](../../Package/format.md) — Package structure reference highlighting which folders get removed.