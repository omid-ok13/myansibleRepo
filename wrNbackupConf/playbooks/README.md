# SSH Cisco Devices Information Gathering

This directory contains the settings and instructions needed to connect to SSH Cisco devices, gather the necessary information, save the running-config as startup-config, create backup file contains the running-config of device with alias name of the device, save it to './backups' directory and save it to a log file.

## Configuration

You can change the `hosts` value to the name of your desired group in the inventory file to run the commands only on that group and not on other devices listed in the inventory file.

### Example:
```yaml
hosts: sw1
```
## Credential

**Author**: Omid Karami  
**Contact**: [o.karami@hotmail.com](mailto:o.karami@hotmail.com)