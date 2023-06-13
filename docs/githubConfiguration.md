# Github Configuration

## Creating PGP Key

In order to sign commits on GitHub, users must create a PGP key. This section provides instructions on how to create a PGP key using KGpg, a graphical key management tool for KDE.

## Prerequisites

Before you begin, make sure you have KGpg installed on your system. You can download KGpg from the official KDE website or your distribution's package manager.

- Official Website: [KGpg](https://apps.kde.org/kgpg/)

## Instructions

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

## Add GPG Key to Your GitHub Account

1. List the long form of your gpg keys
   ```gpg --list-secret-keys --keyid-format=long```
2. Copy the long form of the GPG key ID you'd like to use and paste it in the following command
   ```git config --global user.signingkey <keyID>```
3. Configure github to sign all commits using this key
   ```git config --global commit.gpgsign true```
4. Add your key to `.bashrc` startup file
   ```[ -f ~/.bashrc ] && echo -e '\nexport GPG_TTY=\$(tty)' >> ~/.bashrc```