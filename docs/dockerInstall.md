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

1. Create the Dockerfile
    1. populate with base image
    2. populate install reqs
    3. set the working directory
    4. copy the repo
    5. build the application
    6. define command to run application
2. Create docker image
```azure
docker build -t trust-dns-image .
```

## Move Docker image to Another Machine

First you will save the image as a `.tar` file then transfer it to where ever you need it.
```azure
docker images
docker save -o trust-dns-image.tar trust-dns-image:latest
```
Login to your server using an application such as [FileZilla](https://filezilla-project.org/), locate your `.tar` image file and transfer it to your local machine.

