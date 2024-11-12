# Ansible Configuration Directory
It was a common problem that the current configuration of my Cisco devices was not saved, and after an unexpected reboot, all my configurations were lost. Additionally, I didn't have a backup of the current configuration. To solve this, I created this package to first save my Cisco device configuration and create a backup on my personal desktop. This approach made my job faster, and I hope it does the same for you.

This directory serves as the base directory for all Ansible configuration settings. Follow the instructions below to deploy the playbook to all devices listed in the `inventory` directory.

## Prepare enviroment
### install reqiered software
list:
- ansible
- python3-paramiko
- mutt
- sendmail
- openssh
- git

 ```bash
  sudo apt install ansible python3-paramiko mutt sendmail git openssh
 ```
### configure the ssh
for older cisco devices (2960-*) you need older algos. please check you devices if they use different connection algorithms and cipher, the following worked for me.
please share you experince with me to add it to Docs
just add it to you ~/.ssh/config :

``` ssh condig
Host 192.168.1.*
        PubkeyAcceptedAlgorithms +ssh-rsa
        HostkeyAlgorithms +ssh-rsa
        Ciphers +aes128-cbc
        KexAlgorithms +diffie-hellman-group1-sha1
```
the IP next to `Host` is the range of my ssh address of my devices and the star at the end of it just simply say every address in the network.

### change the needed paths based on you Hierarchie
files, needed to change:
- ./ansible.cfg : `inventory` & `log_path` 
- ./inventory/group_vars/[groupName]/[groupname].yml : `backup_path`

## How to Run the Playbook

To deploy the configuration using the playbook, make sure you're in this directory and execute the following command:

```bash
./ansible > ansible-playbook playbook/playbook.yml --ask-vault-pass
```
When prompted with "vault password," enter your vault password (this is different from your user password).

All changes and outputs will be saved in a log file located at ./logs/ansible.log.

## Support

If you need assistance or have any questions, feel free to email me. I'm happy to help!

## Credential

**Author**: Omid Karami  
**Contact**: [o.karami@hotmail.com](mailto:o.karami@hotmail.com)
