### Description

`gepa` is a wrapper script encompassing many common package manager-related tasks - the purpose intended is to help the user remember how to implement those tasks.

### Usage

```bash
gepa [option] [*package] - package tasks wrapper script
  -b, --binpkg  - binary-archived package create from a pre-compiled inst.
  -c, --cnfdiff - configuration differentiate. Merge old and new configurations.
  -d, --diskcln - disk clean.  rm archives of unused pkg srccode not in tree
  -i, --install - install package
  -i:[b,d,e]    - install: binary, dependency, binary as dependency
  -i:[g,r,s]    - install: get-source only, resume, resume and skip-first
  -i:[u,t,v]    - install: upgrade, total-upgrade (w/ builddeps), revdep-rebld
  -e:[a,b,l]    - edit/view: make.conf, ebuild, elog
  -e:[k,m,n,s]  - edit/view: package.[accept_keywords,mask,unmask,use]
  -f:[e,i,r]    - flag: use flag exclude, include, remove global|cat-name/pkg
  -f:[n,p,q]    - flag: use flag info, package nfo of flags, query pkgs w/ flag
  -g,:[r]       - graph dependencies, reverse dependencies
  -h:a          - help additional
  -l, --list    - list files installed by a package
  -o, --owns    - owning package of a file
  -p:[h,m,n]    - hold a pkg - <=cat/pkg-version>, mask pkg, unmask
  -q, --query   - query for an installed package
  -r, --remove  - remove a package
  -r,:[d,f]     - remove: depclean orphans, force remove pkg (ignores deps)
  -s,:[d]       - search for a package, description with search
  -y, --sync    - sync package (porage tree) database
```

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
