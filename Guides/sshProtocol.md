# SSH Protocol Guide

In this guide we will be reviewing what **SSH Protocol** is,how it works and some typical uses.

## SSH (Secure Shell) and SSH Protocol

SSH, known as Secure Shell or Secure Socket Shell, is a network protocol that gives users a secure way to access a computer over an unsecured network. SSH also can refer to the collection of software utilities that implement the SSH protocol.

Secure Shell provides strong password authentication and public key authentication, as well as encrypted data communications between two computers connecting over an open network. 

SSH is widely used by network administrators for managing systems and applications remotely, enabling them to log in to another computer over a network, execute commands and move files from one computer to another.

Putting it another way SSH protocol is a method for secure remote login from one computer to another. It provides several alternative options for strong authentication, and it protects the communications security and integrity with strong encryption. 

It is a secure alternative to the non-protected login protocols (such as telnet, rlogin) and insecure file transfer methods (such as FTP).

For more information you can watch [this video](https://www.youtube.com/watch?v=Atbl7D_yPug).

## How SSH Protocols work

![image](https://www.google.com/url?sa=i&url=https%3A%2F%2Flinuxapt.com%2Fblog%2Flinux-unix-generating-ssh-keys&psig=AOvVaw2U1SW43RrW6s1_ZpMXPJEs&ust=1631912460137000&source=images&cd=vfe&ved=0CAsQjRxqFwoTCJClwuaxhPMCFQAAAAAdAAAAABAT)

As the image shows it is a secure way that a computer can connect to a server, but how do you connect through the terminal.

In order to establish an SSH connection, you need two components: **a client** and the corresponding **server-side component**. 

- An SSH client is the application you install on the computer which you will use to connect to another computer or a server. (Where the client uses the provided remote host information to initiate the connection) 

- On the server’s side, there is a component called an **SSH daemon** that is constantly listening to a specific TCP/IP port for possible client connection requests. Once a client initiates a connection, the SSH daemon will respond with the software and the protocol versions it supports and the two will exchange their identification data.

Just like seen in the image.

Since creating an SSH connection requires both a client and a server component, you need to make sure they are installed on the local and the remote machine, respectively.

To which you can you can follow [this guide](https://phoenixnap.com/kb/ssh-to-connect-to-remote-server-linux-or-windows) from step 3 to 6.

Once you have done this connecting to a server is very simple you just type this command in your terminal:
`ssh UserName@SSHserver.example.com`

This command will cause the client to attempt to connect to the server named server.example.com, using the user ID UserName. If this is the first time negotiating a connection between the local host and the server, the user will be prompted with the remote host's public key fingerprint and prompted to connect, despite there having been no prior connection:

`The authenticity of host 'sample.ssh.com' cannot be established.` 
`DSA key fingerprint is 01:23:45:67:89:ab:cd:ef:ff:fe:dc:ba:98:76:54:32:10.`
`Are you sure you want to continue connecting (yes/no)?`

Answering yes to the prompt will cause the session to continue, and the host key will be stored in the local system's known_hosts file. This is a hidden file, stored in a hidden directory, called /.ssh/known_hosts, in the user's home directory. Once the host key has been stored in the known_hosts file, the client system can connect directly to that server again without need for any approvals.

## SSH Protocol Typical Uses


