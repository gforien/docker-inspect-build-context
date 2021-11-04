# docker-inspect-build-context

## To Inspect the build context sent to the Docker builder 📦🕵️

### 1. Inspect the working folder with `ncdu`, `gdu`, **WinDirStat** or other

### 2. Clean Docker caches
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~sh
# (!) WARNING : these command will NOT prompt for confirmation
docker builder prune -f
docker image prune -f
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

### 3. Build and launch image `gforien/inspect-context` in the working directory
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~sh
d build . -t gforien/inspect-context -f ./Dockerfile.inspect-context
d run --rm -it gforien/inspect-context
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

### 4. Include more files in the [`.dockerignore`](https://docs.docker.com/engine/reference/builder/#dockerignore-file)
See also [this answer on Stackoverflow](https://stackoverflow.com/a/56086165).


#### Gabriel FORIEN<br>INSA Lyon
