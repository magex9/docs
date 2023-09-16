## Setup

[Installation](https://verdaccio.org/docs/installation/) can be done by installing an npm module globally or setting up a docker container.

Setup the docker container to run in the background.  

> You will lose everything in it if its destroyed, but this is for dev purposes only.

```shell
docker run -it --rm --name verdaccio -p 4873:4873 verdaccio/verdaccio
```

Create a user in the system

> This can be anything and should not be real data

```shell
npm adduser --registry http://localhost:4873/ --auth-type=legacy
```

Now you can publish and packages that are ready to be distributed.

```shell
npm publish --registry http://localhost:4873/ dist/@panel/core
```
