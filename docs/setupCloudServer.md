# Setting up a cloud instance

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
