# Kali-Linux-Dockerfile

Customisable dockerfile to spin up a pre-prepared Kali container

## Included tools

These are the main **tools** which are included:

- Kali Linux [Top 10](https://tools.kali.org/kali-metapackages) metapackage
- exploitdb
- man-db
- dirb
- nikto
- wpscan
- ffuf
- git
- nmap

Note that you can _add/modify/delete_ configuration files by doing the related changes in the dockerfile.

### Usage

In order to build an _image_ from this dockerfile, locate the directory where this file is located and run the following:

```sh
docker build [-t your_image_name] .
```

This will build a docker **image** not a container. To then use the image to create an interactive container, use the following:

``` sh
docker run --tty --interactive < your_image_name >
```

Once you are finished and have exited the container, you can list it using:

``` sh
docker container list --all
```

If you wish to launch the container again, run:

``` sh
docker attach < your_container_ID_or_name >
```

or if it is no longer required:

```sh
docker rm < your_container_ID_or_name >
```

**Godspeed!**
