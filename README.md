# Set up SSH on GitHub
This guide explains how to set up your terminal to work with GitHub.

## Generating a new SSH key
Open git bash
Paste the text below:
```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
This creates a new SSH key, using the provided email as a label
```
Generating public/private rsa key pair
```
When you're prompted to **"Enter a file in wich to save the key"**, press Enter. This accepts the default file location.
```
Enter a file in wich to save the key (~/.ssh/id_rsa.pub): [press Enter]
```
At the prompt, type a secure passphrase.
Once you've created the key, copy the public key to the clipboard:
```
pbcopy < ~/.ssh/id_rsa.pub
```
or
```
clip < ~/.ssh/id_rsa.pub
```

## Adding your SSH key to the ssh-agent
```
eval `ssh-agent -s`
ssh-add ~/.ssh/id_rsa
```

## Add the SSH key to your GitHub account
At Github, click on **Settings** >> **SSH and GPG Keys** >> **New SSH key** >> **Add SSH key**
and paste the key you copy before

## Add the public key to your Account settings
From Bitbucket, choose Personal settings from your avatar in the lower left.

Click SSH keys. If you've already added keys, you'll see them on this page.

Open your .ssh/id_rsa.pub file (or whatever you named the public key file) and copy its contents.
You may see an email address on the last line. It doesn't matter whether or not you include the email address.

From Bitbucket, click Add key.

Enter a Label for your new key, for example, Default public key.

Paste the copied public key into the SSH Key field.

## Clone the repo
Copy the SSH link to clone.
```
git clone link
```
That's all
