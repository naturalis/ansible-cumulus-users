# Ansible Role: Cumulus users

Used to automate user managament on cumulus switches.

This role can change the default credentials of the cumulus user, add some management users with ssh keys and harden ssh access.

Runnable with:
```bash
ansible-playbook playbooks/network/cumulus_users.yml -i inventories/production
```

## Requirements

None.

## Role Variables

Available variables are listed below:
```bash
cumulus_pass: CumulusLinux!
ssh_root_login: without-password
ssh_groups: adm
ssh_port: 22
ssh_pass_auth: 'yes'
admin_users:
- username: testuser
  public_key: AAAAB3blahahahaha
```

## Dependencies

None.

## Example Playbook

    - hosts: switches
      remote_user: cumulus
      gather_facts: no
      become: true
      roles:
        - ansible-cumulus-users

## License

Apache2
