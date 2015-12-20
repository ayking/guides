# Install `npm` packages globally without sudo on OS X and Linux

```sh
mkdir ~/.npm-packages
```

```sh
npm config set prefix '~/.npm-packages'
```

Open or create a ~/.bash_profile file and add this line:

```sh
export PATH=~/.npm-packages/bin:$PATH
```
