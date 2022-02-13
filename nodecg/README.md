# NodeCG base image

## How to use with dependency bundles

For use with dependencies, make your own Dockerfile then add `nodecg install`

```Dockerfile

FROM cma2819/nodecg

RUN nodecg install nodecg install [repo] [--dev]

```

for `nodecg install` usage, read official document [here](https://www.nodecg.dev/docs/installing#installing-bundles).