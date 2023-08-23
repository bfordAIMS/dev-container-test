# Dev container for R

The main file in this repo is `.devcontainer.json`. This sets up a development container using VS Code and Docker with R, zsh and oh-my-zsh. It uses dotfiles from my `.dotfiles` repo to configure zsh and omzsh. 

## How to use

I believe dev containers are only practical (possible?) from VS Code. They set up a development environment within a Docker container based on configuration settings contained in `.devcontainer.json`. The rational behind this particular `.devcontainer.json` is to allow a R development environment (based on my personal preferences) to be setup on top of any `rocker/r-ver` Dockerfile, such that all project related setup is contained in the Dockerfile and all development environment related setup is contained in the `.devcontainer.json` file. This should allow one to place the `.devcontainer.json` file in any folder with a `rocker/r-ver` base Dockerfile and setup a dev container with the click of a button (from within VS Code). 

In my `.zshrc` file I setup the alias 

```shell
alias getDevConR="wget *.devcontainer.json -o $PWD"
```

Then running `getDevConR` from zsh will download the `.devcontainer.json` file into the working directory.


## Test it out

There is also a minimal `Dockerfile` in this repo which installs R. This allows one to clone this repo and immediately get going. It also allows for testing the `.devcontainer.json` file as any problems should not be attributed to the Dockerfile as it only installs R and apt updates.





