# Ansible Role: tcpd

## Description

Manage host access control program

## Requirements

None

## Dependencies

None

## OS Platforms

- RedHat family
- Debian family

## Example Playbook

```
- hosts: all
  roles:
    - tcpd
```

## Role Variables

### tcpd_package_ensure: (string)

```
tcpd_package_ensure: 'present'
```

### tcpd_config_allow: (list)

```
tcpd_config_allow:
  - comment:
    daemon: ALL
    client: ALL
```

### tcpd_config_deny: (list)

```
tcpd_config_deny:
  - comment:
    daemon: ALL
    client: ALL
```

## Example vars

```
tcpd_config_allow:
  - comment:
    daemon: ALL
    client: 127.0.0.1
  - comment:
    daemon: sshd
    client: 192.168.1.0/24

tcpd_config_deny:
  - comment:
    daemon: ALL
    client: ALL
```
