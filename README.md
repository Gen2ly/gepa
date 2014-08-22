### Description

`gepa` is a wrapper script encompassing many common package manager-related tasks - the goal being to aggragate together and help remember how to implement those tasks.

### ToDo

* -f:[e,i,r]  - flag: use flag exclude, include, remove global|cat-name/pkg
* Tests for package category, name, and version (-f,-p)
* euse -[D,E} for flags (unsure about this)
* -p:h parse =cat-name/pkgname-version to cat-name/pkgname (can eix do?)
* -q   define eix options: -Is; "$@" to "$1"?
* -r:f unadded: removebyforce necessary, emerge "$@"???; helpremains
* -h:[a,b] - help additional: part a, and part b
* -i before e ...doh!
* #( ) Block add?

```bash
B | Block )         shift
                    sudo quickpkg $1
                    sudo emerge --unmerge $1
                    sudo emerge $2
                    sudo emerge --usepkgonly --nodeps $1
```

