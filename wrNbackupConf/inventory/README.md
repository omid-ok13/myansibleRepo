# Device Inventory and Group Variables

This directory contains the `<ini>` file, which lists all the devices that need to be managed, as well as the `group_vars` directory, which holds necessary variables for all devices and for each group specifically.

## Instructions

Edit the `myhost.ini` file to add device IP addresses and your alias for each device. The format should look like this:

```ini

[switches]
sw1 ansible_host=192.168.1.10
```

You can change the alias 'sw1' and the IP address as desired.

## Credential

**Author**: Omid Karami  
**Contact**: [o.karami@hotmail.com](mailto:o.karami@hotmail.com)