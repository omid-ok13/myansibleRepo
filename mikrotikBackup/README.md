# Ansible Configuration Directory
It was a common problem that the current configuration of my Cisco devices was not saved, and after an unexpected reboot, all my configurations were lost. Additionally, I didn't have a backup of the current configuration. To solve this, I created this package to first save my Cisco device configuration and create a backup on my personal desktop. This approach made my job faster, and I hope it does the same for you.

This directory serves as the base directory for all Ansible configuration settings. Follow the instructions below to deploy the playbook to all devices listed in the `inventory` directory.

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