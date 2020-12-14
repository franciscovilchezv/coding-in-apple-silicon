# Homebrew installation guide for Apple Silicon

At time of writing this guide, Homebrew for ARM is available but not 100% supported. **You may have to install both in different locations.**

## Homebrew Native installation

We will install the native version in `/opt/homebrew` since it is not 100% functional yet.

1. Create installation directory:

`sudo mkdir -p /opt/homebrew`

2. Change permissions so we don't need `sudo` anymore:

`sudo chown -R $(whoami):admin /opt/homebrew`

3. Install homebrew in there with the script taken from its [official website](https://docs.brew.sh/Installation#untar-anywhere):

```
cd /opt
curl -L https://github.com/Homebrew/brew/tarball/master | tar xz --strip 1 -C homebrew
```

4. Add `brew` (and all tools that we will install with it) to the PATH adding the following line to your `~/.zshrc`:

`export PATH="/opt/homebrew/bin:${PATH}"`

If you don't have a `~/.zshrc`, create one with:

`touch ~/.zshrc`

## Homebrew with Rosetta installation

TBD (pull requests accepted. Don't forget to add an alias to differentiate it from the arm brew)