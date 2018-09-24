# Ansible Role: Cumulus users

Used in [network](https://github.com/naturalis/network/) repo.

Runnable with:
```bash
ansible-playbook playbooks/cumulus_users.yml -i environments/prod
```

This role will configure an extra user for automation.

## Requirements

None.

## Role Variables

Available variables are listed below:
```bash
public_ssh_key: http://172.16.200.254/authorized_keys
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
