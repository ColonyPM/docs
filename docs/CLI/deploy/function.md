# function

Submits a function specification.

## Usage

```bash
cpm deploy function <pkg> <fn-spec>
```

## Aliases

- `func`
- `fn`

## Arguments

| Argument | Description | Required |
|----------|-------------|----------|
| `<pkg>` | Name of the deployed package | yes |
| `<fn-spec>` | the function specification to submit | yes |


## Examples

Submit a function spec named myfn.json from mypkg:

```bash
cpm deploy function mypkg myfn
```
