# Credential and Encrypted Password Files

This directory contains credentials and encrypted password files for all devices.

## User Configuration

You should change the `ansible_user` value to your desired username that has access to your devices. At least privilege level 5 is required.

### Example:
```yaml

ansible_user: your_username
```

Password Options

You can either enter your password as the value for ansible_password (not recommended):


```yaml

ansible_password: mypassword
```


Use an encrypted password file (vault) to securely store your password by following these steps:

- First, edit the mypassword file to include your password and save it.
- Run the following command in the directory:

```bash

ansible-vault encrypt ./mypass
```
- Enter a vault key when prompted.
- Delete your clear text password file.
- Done.

## Credential

**Author**: Omid Karami  
**Contact**: [o.karami@hotmail.com](mailto:o.karami@hotmail.com)