# Ram disk

```sh
diskutil erasevolume HFS+ 'RAM' `hdiutil attach -nomount ram://8388608`
```
# Homebrew
```sh
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

# codesign
```sh
codesign --verify --verbose [path]
```

# Gatekeeper
```sh
spctl --assess -vv [path]
```
