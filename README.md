# OpenShift.AWS

`OpenShift.AWS` is a ansible playbook to install a OpenShift Enterprise 3.2 in AWS. 
Default number of nodes is `1` master and `2` slave nodes. All variables are stored in the `group_vars/all` file. This includes secrets like AWS API keys and Red Hat subscription info. This playbook also assumes that you will be using your own domain name and have it registered already in AWS. This allows the playbook to use subdomains for all OSE nodes, `master.ose.<yourdomain>.io`. 

# Dependencies

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


## Provision in AWS 
`ansible-playbook -i inventory --private-key=id_rsa site.yml`


# Demo

Scale up pods in console

oc get
oc get pods
oc login
oc get pods
oc delete pod nodejs-example-1-02re8