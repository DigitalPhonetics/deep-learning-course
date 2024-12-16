# Integrated Development Environment (IDE)

## IDEs for Python Development

You can choose your preferred IDE but we can support you best with issues regarding VS code.

- **PyCharm**
    - Offers code analysis, a graphical debugger, an integrated unit tester, and support for web development with Django.

- **Visual Studio Code**
    - Supports Python through extensions, and offers features like debugging, IntelliSense, and Git integration.

Other options:

- **Spyder**
- **Atom**
- **Sublime Text**
- **Thonny**
- **Eclipse with PyDev**

## Remote SSH Connection with VS Code
To work on your projects remotely, you can use the Remote - SSH extension in Visual Studio Code. 
This allows you to connect to a remote server via SSH and use VS Code as if you were working locally. 

https://code.visualstudio.com/docs/remote/ssh

### Steps to Set Up Remote SSH in VS Code

1. **Install the Remote - SSH extension**: Go to the Extensions view in VS Code and search for "Remote - SSH". Install the extension provided by Microsoft.

2. **Add a new SSH host**: Open the Command Palette (`Ctrl+Shift+P`), type `Remote-SSH: Add New SSH Host`, and enter your SSH connection string (e.g., `user@hostname`).

3. **Configure SSH settings**: You may be prompted to select the SSH configuration file to update. Choose the appropriate file (usually `~/.ssh/config`).

4. **Connect to the SSH host**: After adding the host, open the Command Palette again, type `Remote-SSH: Connect to Host`, and select the host you added.

5. **Open a remote folder**: Once connected, you can open any folder on the remote machine and start working on your code.

## Copying SSH Public Key to Remote Server

To enable passwordless authentication, you need to copy your SSH public key to the remote server. 
For more detailed instructions, refer to the official documentation: https://www.ssh.com/academy/ssh/copy-id

Follow these steps:

1. **Generate an SSH key pair**: If you don't already have an SSH key pair, generate one using the following command:
    ```sh
    ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
    ```
    Follow the prompts to save the key pair in the default location (`~/.ssh/id_rsa`).

2. **Copy the public key to the remote server**: Use the `ssh-copy-id` command to copy your public key to the remote server:
    ```sh
    ssh-copy-id user@hostname
    ```
    Replace `user` with your username and `hostname` with the remote server's address.

3. **Verify SSH key authentication**: Test the connection to ensure that the SSH key authentication is working:
    ```sh
    ssh user@hostname
    ```
    You should be able to connect to the remote server without being prompted for a password.
