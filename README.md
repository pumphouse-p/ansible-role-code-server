# Ansible Role: Code Server

An Ansible role that deploys [Code Server](https://github.com/coder/code-server).

# Requirements

None.

# Role Variables

| Variable Name                 | Default Value | Required                                             | Description                                                 | Example  |
|:-----------------------------:|:-------------:|:----------------------------------------------------:|:-----------------------------------------------------------:|:--------:|
| `code_server_package_state`   | `present`     | No                                                   | State of package on systems.                                |          |
| `code_server_package_version` | `latest`      | No                                                   | Version to install.                                         | `4.2.0`  |
| `code_server_user`            | ''            | Yes                                                  | User that should have an instance of code-server available. | `myuser` |
| `code_server_auth_password`   | `password`    | Password used to authenticate in the code-server UI. | `myplaintextpassword`                                       |

# Dependencies

None.

# Example Playbook

```yaml
- hosts: all
  vars:
    code_server_user: myuser
    code_server_auth_password: myplaintextpassword

  roles:
    - pumphouse_p.code_server
```

# License

GPL

# Author Information

Devin Parrish ([GitHub](https://github.com/pumphouse-p))
