# Basic traefik connected container setup

This setup allows you to run react project in both **DEV** and **PROD** modes using docker environment.
> If you want to use `npm` instead, just replace all `yarn` instances to corresponding npm commands

---

To start **developing** react you should firstly install all packages in `node_modules` folder locally and only after that start docker container.

**Production** mode doesn't require `node_modules` folder.

#### Start **development** mode
1. `yarn install` or `yarn`
2. `./docker-scripts.sh`

#### Start **production** mode
`./docker-scripts.sh prod`
> Add `-d` to run container detached

#### Start **production** mode with recreating react `build` folder
`./docker-scripts.sh prod:build`
> Add `-d` to run container detached

#### Stop running **production** container
`./docker-scripts.sh stop`