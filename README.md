# Set up SSH on GitHub
This guide explains how to set up your terminal to work with GitHub.

## Generating a new SSH key
1. Open git bash
2. Paste the text below:
```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
3. This creates a new SSH key, using the provided email as a label
```
Generating public/private rsa key pair
```
4. When you're prompted to **"Enter a file in wich to save the key"**, press Enter. This accepts the default file location.
```
Enter a file in wich to save the key (~/.ssh/id_rsa.pub): [press Enter]
```
5. At the prompt, type a secure passphrase.
6. Once you've created the key, copy the public key to the clipboard:
```
pbcopy < ~/.ssh/id_rsa.pub
```
or
```
clip < ~/.ssh/id_rsa.pub
```

## Adding your SSH key to the ssh-agent
1. Add your SSH key to the SSH agent:
```
ssh-add ~/.ssh/id_rsa.pub
```

## Add the SSH key to your GitHub account
1. Add your SSH key to the SSH agent:
```
ssh-add ~/.ssh/id_rsa.pub
```
2. At Github, click on **Settings** >> **SSH and GPG Keys** >> **New SSH key** >> **Add SSH key**

## Clone the repo
1. Copy the SSH link to clone.
```
git clone link
```
That's all
