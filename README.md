Code of conduct
---------------

The main ideas of this org's Dockerfiles:
* Dockerfiles for security applications.
* Apps in container start as non-root user only.
* Base image on Alpine if possible.
* The number of layers is minimal and the cache is optimized - rebuild
  only needed layers.
* Multistage builds are preferred; we use buildkit `DOCKER_BUILDKIT=1` to
  build images.

How to contribute your Dockerfile
---------------------------------

* Create an issue here with a link and a short description.

How to use those dockers
------------------------

All images are uploaded as automated builds to the official docker hub under
[ilyaglow](https://hub.docker.com/u/ilyaglow) user (this will probably change
in the future).

But I encourage you to build all containers by yourself. Keep in mind
supply-chain attacks and reduce your attack surface.

You should be able to build a single Dockerfile repository with a command like
this:
```
docker build -t imgname https://github.com/security-dockerfiles/repo.git
```

For docker-compose repositories just use good old `git clone` and
`docker-compose up - d` then.
