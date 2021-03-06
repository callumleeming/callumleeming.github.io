---
layout: default
title: "Linux Password-less Authentication"
blogs: blog1
---

# What is Password-less Authentication?
SSH Password-less Authentication is basically having the ability to log-on to another remote server without having to enter a password. This is particularly useful when you want to automate tasks/jobs such as zipping-up a directory by using a script, or even for remote command execution.

You should consider using SSH password-less authentication when you are dealing with a number of remote servers. By adding public keys to a file, you can eliminate the whole process of exposing a password elsewhere.

Using Password-less authentication now means we don’t have to put our passwords in continuous integration. Therefore meaning that we don’t need to share passwords between team members, thus making the password less accessible.

---

## Why start using Password-less Authentication
In some cases, you may need to use Password-less Authentication for running commands on a remote server. Before having Password-less Authentication setup on the server, you probably would have used a password that was being stored / remembered somewhere. This is not very secure as the password could easily be found. However, once you have setup the Password-less Authentication, the key is less accessible, therefore making it a lot more secure.


---

## Passwords Vs Keys
Passwords are strong right? Doing some research suggested that they can take seconds to crack if they do not contain any special characters, capital letters or numbers.

`RSA Keys` - It would take approximately 1.5 million years with a standard desktop machine to crack a 2048 bit key.

`Passwords` - It would take roughly 6 months with a standard desktop machine to crack a 10 character password containing special characters.

---

## How to set it up
First of all, you will need the SSH keys for the server that you’re using.

Log onto the box you want to connect to
Navigate to `~/.ssh/`
Copy the `public key` into the `authorized_keys` file by running this command `ssh-copy-id -i ~/.ssh/mykey user@host`
If the SSH keys need to be regenerated, then you will need to follow these steps:

1) Logon to the box that you want to connect from
2) If it’s a different user, impersonate using 
`sudo su - username`
3) In the home directory, run
`ssh-keygen -r rsa`
4) Don’t set a password
5) It will generate the file at `HomeDirectory/.ssh/id_rsa.pub`
6) You will need the public key to be added to the box you want to connect to 
You should now be able to ssh onto the box from the client machine, without the password. 
e.g. `ssh username@hostname dir`

### Post by: **Callum Leeming, Junior Software Developer**
