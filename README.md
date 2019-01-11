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
