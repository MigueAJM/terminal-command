# **What is SSH?**

## _(Secure shell)_. It is a protocol that facilitates secure communication between two systems using a client/server architecture, managing to connect to a remote host.

## _encryption techniques_

### - **symmetric encryption**

#### Symmetric encryption is a form of encryption in which a secret key is used for both encryption and decryption of a message, by both the client and the host **(shared key)**.

### - **asymmetric encryption**

#### uses two separate keys for encryption and decryption. These two keys are known as the **public key** and the **private key**.

### - **Hashing**

#### **One-way hash** functions differ from the previous two forms of encryption in that they are never meant to be cracked. They generate a single value of a fixed length for each entry that does not show a clear trend that can be exploited. This makes them virtually impossible to reverse.

#### _algorithm_

- ed25519
- ECDSA
- rsa -b 4096 "_size above 4096 is recommended_"

### **create ssh keys**(generate public_key and private_key)

#### `-t rsa` algorithm type, `-b 4096` bit length, `-f ~/.ssh/file_name` specifies name of key files to generate and `-C "your_email@example.com"` comment

- `> ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`
- `> Enter a file in which to save the key (/c/Users/you/.ssh/id_algorithm):[Press enter]`
- `> Enter passphrase (empty for no passphrase): [Type a passphrase]`
- `Enter same passphrase again: [Type passphrase again]`

### **testing your SSH connection**

- `ssh -T git@github.com`
- `ssh -T git@gitlab.com`
- `ssh -T git@bitbucket.com`
