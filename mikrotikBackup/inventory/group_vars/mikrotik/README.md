# Mikrotik Configuration

This directory contains the `mikrotik.yml` file, which is used for configuring Mikrotik devices in our network.

## mikrotik.yml

The `mikrotik.yml` file includes various settings and parameters required for the proper connection to Mikrotik devices. Below is a brief overview of the key sections and parameters:

### Parameters

- **ansible_user**: The username used for accessing the Mikrotik device.
- **ansible_ssh_pass**: The password used for accessing the Mikrotik device.

### Example

```yaml
---
ansible_connection: ansible.netcommon.network_cli
ansible_network_os: community.routeros.routeros
ansible_user: "ansible"
ansible_ssh_pass: "123456789"
ansible_command_timeout: 120

backup_path: "./path/to/backupDir"
```

## Usage

To apply the configuration defined in `mikrotik.yml`, use the appropriate playbook or command that references this file. Ensure that all parameters are correctly set to match your network requirements.

For more detailed information on Mikrotik configuration, refer to the official Mikrotik documentation.

## Contact

For any questions or support, please contact:

- **Name**: omid karami
- **Email**: [okarami79@hotmail.com]