

<samp>

# [add-SSH-keys-linux]()

[![Made in Tanzania](https://img.shields.io/badge/made%20in-tanzania-008751.svg?style=flat-square)](https://github.com/Tanzania-Developers-Community/made-in-tanzania)

How to successfully add ssh keys to your linux machine and connect them to your GitHub account)


## Key Generation

Paste the command below and add an email address linked to your github account.

```bash
1. $ ssh-keygen -t ed25519 -C "your-github-email-address"
    Enter file in which to save the key (/home/username/.ssh/id_ed25519):
    Enter passphrase (empty for no passphrase): 
    Enter same passphrase again:
```
NB:
    -You can presse enter throughout to use defaults.
        or 
    -You will then be prompted to enter the path and name of your existing or new file you need to save your ssh key. for instance /home/username/.ssh/file-name where [file-name] is the name if the file you need to save your ssh key. Then press enter.

Appearance of your terminal

```bash
# Your keys appear like this
The key fingerprint is:
SHA256:7bHf5wcoraPjaAO5thuS7TjiQC/rFEfProfh/U811cQ your-github-email-address
The key's randomart image is:
+--[ED25519 256]--+
|               ..|
|               oE|
|  . .         . .|
| . o o   .   .   |
|  + =.o S o.o.   |
|   @++   ..+o..  |
|  =.=*o   +o   . |
| o .=+=...o. .  o|
|  ..+=.+++... .oo|
+----[SHA256]-----+
```

       
## Start the ssh-agent in the background

```bash
    $ eval "$(ssh-agent -s)"
```

## Add your SSH private key to the ssh-agent. 

```python
 $ ssh-add ~/.ssh/
```

## Display the existing or newly made ssh key

Cop the output and follow the steps to add SSH Key to github.

```bash
    $ cat ~/.ssh/file-name.pub
        ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIDEgJhakH0sUfyWwaoSBCgDIanMDBDxea3VcpxJZTjZJ your-github-email-address
```

## Adding SSH Key to GitHub

Steps:
1. Go to Settings
2. SSH and GPG Keys
3. On SSH Keys click New SSH Key
4. Add the name of the key and paste the private ssh key here.
5. Click Add SSH Key


## Contributing

This is an opensource project under ```MIT License``` so any one is welcome to contribute from typo, to source code to documentation, ```JUST FORK IT```.
    
## References 
1. [Github SSH Docs](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)


## All the credit

1. [zipa-tech](https://github.com/zipa-tech)
2. All other contributors
</samp>