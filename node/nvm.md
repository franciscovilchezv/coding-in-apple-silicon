# NVM

Installation of node with nvm is very straighforward. **No Rosetta usage is needed at all**.

- Create the `~/.zshrc` in you don't have it yet by doing:

`touch ~/.zshrc`

- Run installation script from their [official installation guide](https://github.com/nvm-sh/nvm#installing-and-updating). At the time of writing this guide, the following command worked correctly:

`curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.2/install.sh | bash
`

- You can see that *nvm* was installed in `~/.nvm`. **You may also verify that your `./zshrc` now includes the path for nvm on it.** In case it does not, you can include it manually. It is the one at the end of the [Install & Update script section](https://github.com/nvm-sh/nvm#install--update-script). 

- For installing latest node version, you can run:

`nvm install node`

- An alias for `node` and `npm` command are automatically created. Global binaries are created in a file hierarchy inside `~/.nvm`. You can now use `npm` and `node` natively in M1.