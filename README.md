# Informal Task 

## Setting up a DNS Server

_Disclaimer: Some of the basic setup instructions, such as creating a GPG key and setting up an instance on Vultr, were sourced from the web and slightly modified for the purposes of this documentation._

### Github Configuration

#### Creating PGP Key

In order to sign commits on GitHub, users must create a PGP key. This section provides instructions on how to create a PGP key using KGpg, a graphical key management tool for KDE.

#### Prerequisites

Before you begin, make sure you have KGpg installed on your system. You can download KGpg from the official KDE website or your distribution's package manager.

- Official Website: [KGpg](https://apps.kde.org/kgpg/)

#### Instructions

1. Launch KGpg 

Open KGpg from your applications menu or by executing the kgpg command in the terminal.

2. Generate a new key pair

- Click on "Keys" in the menu bar and select "New Key Pair".
- Enter your name and email address. Optionally, you can add a comment.
- Choose the key type and key size. RSA is a common choice.
- Set an expiration date for the key if desired.
- Click "Next" to proceed.
- Select a secure passphrase for your key. Make sure to choose a strong and memorable passphrase. 
- Click "Next" to generate the key pair. 

3. Export the public key

- In KGpg, select your newly created key from the key list.
- Right-click on the key and choose "Export Public Key".
- Save the public key to a file with the .asc extension.

#### Add GPG Key to Your GitHub Account

1. List the long form of your gpg keys
```gpg --list-secret-keys --keyid-format=long```
2. Copy the long form of the GPG key ID you'd like to use and paste it in the following command
```git config --global user.signingkey <keyID>```
3. Configure github to sign all commits using this key
```git config --global commit.gpgsign true```
4. Add your key to `.bashrc` startup file
```[ -f ~/.bashrc ] && echo -e '\nexport GPG_TTY=\$(tty)' >> ~/.bashrc```


### Building The Application

To build the application, the developer needs to clone the repository and follow the installation instructions. These instructions may vary depending on the chosen operating system for the build. To contribute to the project, the user should fork the repository and develop from their own branch. However, for the purpose of this task, we will only be building the application for personal use.

Since this task involves building clusters that communicate with each other, I have chosen to set up cloud instances. I started with one instance initially and added the additional virtual machine (VM) towards the end of the project.

#### Setting up a cloud instance

The process may vary depending on the service the user chooses to utilize. In my example, I will be setting up an instance using [Vultr](https://www.vultr.com/)

1. Sign up for a Vultr account:

Visit the Vultr website and sign up for an account if you don't already have one. Provide the required information and complete the registration process.

2. Log in to the Vultr dashboard:

Once you have an account, log in to the Vultr dashboard using your credentials.

3. Create a new server:

- Click on the "Servers" tab in the navigation menu.
- Click on the blue "Deploy New Server" button.

4. Configure the server settings:

- Choose a server location that is geographically closest to your target audience or your preferred location.
- Select a server type. Vultr offers various options such as Compute Instances, Bare Metal, and High Frequency Compute.
- Choose an appropriate server size based on your requirements, such as CPU, RAM, and storage.
- You can optionally enable additional features like IPv6, Private Networking, and backups.

5. Choose an operating system:

- Select your preferred operating system for the server. Vultr offers a wide range of options including various Linux distributions and Windows Server versions.
- You can also choose to deploy from a snapshot, upload your own ISO, or use a startup script.

6. Set a server hostname:

- Provide a hostname for your server. This can be any name of your choice.

7. Deploy the server:

- Review your server configuration settings.
- Once you're ready, click on the "Deploy Now" button to initiate the deployment process.

8. Access and manage your server:

- Once the deployment is complete, you will receive the server's IP address and login credentials.
- Use a SSH client or a remote desktop client to connect to the server using the provided credentials.
- You can now install and configure any desired software or services on your Vultr cloud server.


When setting up an instance, it is typically important to configure additional security settings beyond SSH. These settings may include customizing the SSH configuration file to disallow root access or password-based authentication. Additionally, it is recommended to set up a firewall to restrict access to specific ports and create a non-root user for system administration. However, for the purpose of this project, I have skipped these security protocols to save time.

### Building the Application
