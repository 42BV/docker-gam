[![Docker Build Statu](https://img.shields.io/docker/build/42bv/gam.svg)](https://hub.docker.com/r/42bv/gam/builds/) ![Docker Stars](https://img.shields.io/docker/stars/42bv/gam.svg) [![Docker Pulls](https://img.shields.io/docker/pulls/42bv/gam.svg)](https://hub.docker.com/r/42bv/gam/)

# Docker - Google Apps Manager (GAM)

GAM is a command line tool for Google Apps administrators to manage domain and user settings

---

## Docker

### Supported tags and Dockerfile

- `latest` [(Dockerfile)](https://github.com/42BV/docker-gam/blob/master/Dockerfile)


### Pull  

Get the latest version:
```
docker pull 42bv/gam:latest
```

### Build  

Clone the repository:
```
git clone git@github.com:42BV/docker-gam.git
cd docker-gam
```

Build the current Dockerfile  and tag the image:   
```
docker build -t gam .
```

### Run

Make sure you have the required credential files in your current directory:
- `oauth2.txt`
- `oauth2service.json`
- `client_secrets.json`

*You need to generate these first, see installation.*
```
docker run -it --rm \
       -v "${PWD}"/oauth2.txt:/opt/gam/src/oauth2.txt" \
       -v "${PWD}"/oauth2service.json:/opt/gam/src/oauth2service.json \
       -v "${PWD}"/client_secrets.json:/opt/gam/src/client_secrets.json \
       --name gam 42bv/gam
```

---

## License

Released under the [MIT license](https://github.com/42BV/docker-gam/blob/master/LICENSE.md).