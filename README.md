# Informal Task 

## Setting up a DNS Server

_Disclaimer: Some of the basic setup instructions, such as creating a GPG key and setting up an instance on Vultr, were sourced from the web and slightly modified for the purposes of this documentation._

### Github Configuration

Some initial setup may be required to use PGP for signing commits. Below is a link to the steps I took to accomplish this:

1. [Github Configuration](docs/githubConfiguration.md)

### Building The Application

Since this task involves building clusters that communicate with each other, I have chosen to set up cloud instances. I started with one instance initially and added the additional virtual machine (VM) towards the end of the project.

**Server Specs:**
```
Regular Performance Intel Cloud Compute Share vCPU
4 vCPU
8 gb RAM
160gb SSD
Ubuntu 22.04
```

2. [Setting up a cloud server](docs/setupCloudServer.md)

Next, we will proceed to build the application on our newly configured virtual machine (VM).

3. [Building the Application](docs/buildApp.md)
   
After completing the build using Cargo, we will want to transpose the application into a Docker image.

5. [Install Docker](docs/dockerInstall.md)

