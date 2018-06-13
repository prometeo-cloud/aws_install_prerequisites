# aws_prerequisites

## Description:

This role installs AWS dependencies:

- awscli
- boto
- boto3

## Behaviour:

**Feature:** Install AWS dependencies
- **Given** an Ansible Control Node or Ansible Tower is configured
- **When** the role is executed
- **Then** the AWS pre-requisites are installed

## Configuration:

Variables specific to this role:

| Variable | Description | Example |
|-----|-----|-----|
| **required_packages** | List of packages to install. | [see vars/main.yml](vars/main.yml) |
| **pip_packages** | List of Python modules to install. | [see vars/main.yml](vars/main.yml)  |

## Usage:

How to invoke the role from a playbook:

```yaml
- name: Installing AWS pre-requisites
  include_role:
    name: "aws_install_prerequisites"
```
