# Brief SSH Introduction
Secure Shell (SSH) is a cryptographic network protocol used for secure data communication, remote command-line login, remote command execution, and other secure network services between two networked computers. It provides a secure channel over an unsecured network by using a client-server architecture, connecting an SSH client application with an SSH server.

While SSH is a powerful tool, in the following we briefly cover connecting to SSH hosts in a terminal.

Command to connect to an SSH host:
`ssh username@hostname.ims.uni-stuttgart.de`

Viable hostnames for the IMS student servers:
- `strauss` GPUs available
- `nandu` GPUs available
- `kiwi` GPUs available
- `phoenix` CPU only
- `dodo` CPU only

Also check out further information on SSH with [VS Code](ide.md#remote-ssh-connection-with-vs-code).

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
