# upload

Uploads a package to the [Colony PM registry](https://colonypm.xyz).

## Usage

```bash
cpm pkg upload [PATH] --token <TOKEN>
```

## Arguments

| Argument | Description | Required |
|----------|-------------|----------|
| `[PATH]` | Path to the package directory | No |

## Flags  

| Flag | Description | Required |
|------|-------------|----------|
| `--token <TOKEN>` | Authentication token used to authorize the upload | Yes |

A token is a string that is used to authenticate the user. To generate a token, visit the [Colony PM registry](https://colonypm.xyz) and log in.

## Examples

Upload the current directory:

```bash
cpm pkg upload --token 4:1vU5si:x_4jtJYfwUCg0JJgiI95rXTOPbtrVlZkM_AyQBtezMk

```
Upload a specific package directory:

```bash
cpm pkg upload /path/to/package --token 4:1vU5si:x_4jtJYfwUCg0JJgiI95rXTOPbtrVlZkM_AyQBtezMk
```
