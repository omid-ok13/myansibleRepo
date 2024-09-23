# Ansible Configuration Directory
I wanted to create documentation for one of my projects involving a large number of Cisco switches. I used Ansible to gather information such as image version, switch type, model, and all trunk interfaces of each switch. This approach made my job faster, and I hope it does the same for you.

This directory serves as the base directory for all Ansible configuration settings. Follow the instructions below to deploy the playbook to all devices listed in the `inventory` directory.

## How to Run the Playbook

To deploy the configuration using the playbook, make sure you're in this directory and execute the following command:

```bash
./ansible > ansible-playbook playbook/playbook.yml 
```

All changes and outputs will be saved in a log file located at ./logs/ansible.log.

## Support

If you need assistance or have any questions, feel free to email me. I'm happy to help!

## Credential

**Author**: Omid Karami  
**Contact**: [o.karami@hotmail.com](mailto:o.karami@hotmail.com)