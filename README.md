# Set up SSH on GitHub
This guide explains how to set up your terminal to work with GitHub.

## Generating a new SSH key
1. Open git bash
2. Paste the text below:
```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
3. This creates a new ssh key, using the provided email as a label
```
Generating public/private rsa key pair
```
4. When you're prompted to "Enter a file in wich to save the key", press Enter. This accepts the default file location.
5. At the prompt, type a secure passphrase.
