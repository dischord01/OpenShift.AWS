# OpenShift.AWS

`OpenShift.AWS` is a great ansible playbook.

# Dependencies

`/etc/ansible/hosts` needs to have entry for localhost. 

```
localhost ansible_connection=local
```

Terraform needs to be installed locally

OSX
```
brew install terraform
```


# Install Ansible Roles from [Galaxy](https://galaxy.ansible.com/)

```
ansible-galaxy install username.rolename
```


# Usage

## Development (if you used `--vagrant` flag: `vagrant up`

Run `vagrant provision` to provision your vms with Ansible.

## Production
`ansible-playbook -i inventory site.yml`


