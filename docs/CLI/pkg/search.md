# search

Search packages on the repository from the terminal. Indexes package name, descriptions and authors. 


## Usage

```bash
$ cpm pkg search <query>
```


## Examples

```bash
$ cpm pkg search fibbers
fibbers
```
Returned one package named fibbers.


```bash
$ cpm pkg search "A package"
fibbers
fibbig
01-getting-started
...
```
Returned all packages with the phrase "A package" in its description. 


```bash
$ cpm pkg search doesntexist
No packages found.
```
No packages matched the "doesntexist" query.
