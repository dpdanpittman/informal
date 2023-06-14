# Building the Application

To build the application, the developer needs to clone the repository and follow the installation instructions. These instructions may vary depending on the chosen operating system for the build. To contribute to the project, the user should fork the repository and develop from their own branch. However, for the purpose of this task, we will only be building the application for personal use.

1. Clone the [repository](https://github.com/bluejekyll/trust-dns)
```git clone https://github.com/bluejekyll/trust-dns```
2. Follow build instructions
   1. Install Prerequisites 
         ```bash
      sudo apt install openssl
      sudo apt install libssl-dev pkg-config
      ```
      1. Install [rust](https://www.rust-lang.org/) cargo
      
      ```bash
      sudo apt install cargo
      ```
   3. Build Trust-DNS
   ```bash
   cargo build --release --all-features -p trust-dns
   ```