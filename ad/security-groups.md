# Active Directory Security Groups

This document describes the security groups created in the Active Directory environment.

## Security Groups

| Group             | Scope  | Type     | Description                                                                |
| ----------------- | ------ | -------- | -------------------------------------------------------------------------- |
| **IT-Admins**     | Global | Security | Members have administrative privileges for IT systems and user management. |
| **HR**            | Global | Security | Members can access Human Resources resources and shared folders.           |
| **Finance**       | Global | Security | Members can access Finance department resources and financial data.        |
| **VPN-Users**     | Global | Security | Members are permitted to connect to the corporate VPN.                     |
| **Server-Admins** | Global | Security | Members have administrative access to Windows servers.                     |

## Configuration

* **Group Scope:** Global
* **Group Type:** Security

## Best Practices

* Assign permissions to **groups**, not individual users.
* Add users to the appropriate group based on their role.
* Follow the principle of least privilege by granting only the permissions required.

