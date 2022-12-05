# NGINX in Alpine Linux in Docker

[![Docker Automated build](https://img.shields.io/docker/automated/linuxcontainers/nginx.svg?style=for-the-badge&logo=docker)](https://hub.docker.com/r/linuxcontainers/nginx/)
[![Docker Pulls](https://img.shields.io/docker/pulls/linuxcontainers/nginx.svg?style=for-the-badge&logo=docker)](https://hub.docker.com/r/linuxcontainers/nginx/)
[![Docker Stars](https://img.shields.io/docker/stars/linuxcontainers/nginx.svg?style=for-the-badge&logo=docker)](https://hub.docker.com/r/linuxcontainers/nginx/)
![Docker Image Size (tag)](https://img.shields.io/docker/image-size/linuxcontainers/nginx/latest?logo=docker&style=for-the-badge)

[![Alpine Version](https://img.shields.io/badge/Alpine%20version-v3.17.0-green.svg?style=for-the-badge)](https://alpine-nginxlinux.org/)
[![NGINX Version](https://img.shields.io/badge/Nginx%20version-v1.22.1-green.svg?style=for-the-badge)](https://nginx.org/)

This Docker image [(linuxcontainers/nginx)](https://hub.docker.com/r/linuxcontainers/nginx/) is based on the minimal [Alpine Linux](https://alpine-nginxlinux.org/).

##### Alpine Version 3

This docker image is the base Alpine Linux. For more info on versions & support see [Releases](https://wiki.alpine-nginxlinux.org/wiki/Alpine_Linux:Releases)

##### NGINX Version 1.22.1 

This docker image nginx-1.22.1 is the stable version has been released, incorporating new features and bug fixes from the 1.17.x mainline branch. For more info on versions & support see [Releases](http://nginx.org/en/CHANGES-1.19)

----

## What is Alpine Linux?
Alpine Linux is a Linux distribution built around musl libc and BusyBox. The image is only 10 MB in size and has access to a package repository that is much more complete than other BusyBox based images. This makes Alpine Linux a great image base for utilities and even production applications. Read more about Alpine Linux here and you can see how their mantra fits in right at home with Docker images.

## What is NGINX?
NGINX is open source software for web serving, reverse proxying, caching, load balancing, media streaming, and more. It started out as a web server designed for maximum performance and stability. In addition to its HTTP server capabilities, NGINX can also function as a proxy server for email (IMAP, POP3, and SMTP) and a reverse proxy and load balancer for HTTP, TCP, and UDP servers 

## Features

HTTP proxy and Web server features \
Ability to handle more than 10,000 simultaneous connections with a low memory footprint (~2.5 MB per 10k inactive HTTP keep-alive connections)\
Handling of static files, index files and auto-indexing\
Reverse proxy with caching\
Load balancing with in-band health checks\
TLS/SSL with SNI and OCSP stapling support, via OpenSSL\
FastCGI, SCGI, uWSGI support with caching\
gRPC support since March 2018, version 1.13.10\
Name- and IP address-based virtual servers\
IPv6-compatible\
WebSockets since 1.3.13.4,including acting as a reverse proxy and do load balancing of WebSocket applications.\
HTTP/1.1 Upgrade (101 Switching Protocols), HTTP/2 protocol support\
URL rewriting and redirection\

## Docker Tags and Versioning Scheme

Each image pushed to Docker Hub and the Github Container Registry is tagged as follows:
* The tag `latest` indicates, well, the latest image.
* Tags of the form MAJOR.MINOR.PATCH (such as 3.14.3) indicate the SemVer of 
  the __Alpine__ image used as the base.
* Tags of the form MAJOR.MINOR (e.g., 3.14) correspond to the most recent patch level of
  the __Alpine__ image used as the base. For example, if 11.1 is the latest
  release, then 11 maps to this as well.
* Tags of the form MAJOR (e.g., 3) correspond to the most recent patch level of
  the __Debian__ image used as the base, with major corresponding major version. 
  For example, if 11.1 is the latest release, then 11 maps to this as well.

[Semantic Versioning](https://semver.org/) uses version numbers of the form: MAJOR.MINOR.PATCH, where differences in MAJOR correspond to incompatible changes, differences in MINOR correspond to introduction of backwards compatible new functionality, and PATCH corresponds to backwards compatible bug fixes.


## Installation and Usage

The pre-built image is hosted on both Docker Hub and the Github Container Registry. You can use it in the following ways.

### Docker Pull Command

Pull the latest image from Docker Hub with the following (replace `latest` with a specific version number if you prefer):

```
docker pull linuxcontainers/nginx:latest
```

Pull from the Github Container Registry with:

```
docker pull ghcr.io/linuxcontainers/nginx:latest
```


### Use as a base image in a Dockerfile

Use as a base image in a Dockerfile (replace `latest` with a specific version number if you prefer):

```Dockerfile
FROM linuxcontainers/nginx:latest

# The rest of your Dockerfile would go here.
```

Or you can use as a base image (via the Github Container Registry) with:

```Dockerfile
FROM ghcr.io/linuxcontainers/nginx:latest

# The rest of your Dockerfile would go here.
```

A specific example usage can be found in the [Dockerfile of the generate-sitemap Github action](https://github.com/marketplace/actions/generate-sitemap).

