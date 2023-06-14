# Transposing an application into a docker image

I am using Ubuntu 22.04 as my Linux version. To install Docker on this fresh machine, I followed the guide provided by DigitalOcean: [How to Install and Use Docker on Ubuntu 22.04.](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-22-04)

### Useful Tips when Installing Docker

- Check to make sure Docker was succesfully installed and is running
```azure
sudo systemctl status docker
```
- Set up "Executing the Docker Command Without Sudo"
- Check help commands by running:
```azure
docker
```

## Dockerize the Application

1. Create the docker image including the pre-reqs