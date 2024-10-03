# test-ansible-main-project

This is test Ansible main project using Ansible collections

This project make use of other repositories:

[test-ansible-role](https://github.com/szymon-m/test-ansible-role)

[test-ansible-collection](https://github.com/szymon-m/test-ansible-collection)

## Possible structure of project

- /home/ansible
  - test-ansible-main-project/       <----- this project from [Github](https://github.com/szymon-m/test-ansible-main-project)
  - inventory/                       <----- inventory
    - hosts_vars/                    <----- Ansible host_vars directory
    - hosts
  - venv-ansible/                    <----- Python virtual environment directory

## Inventory

Create link for host_vars folder and hosts file in project root to inventory
- /home/ansible/test-ansible-main-project/hosts -> /home/ansible/inventory/hosts
- /home/ansible/test-ansible-main-project/host_vars -> /home/ansible/inventory/host_vars

## To install and user roles

1. `cd test-ansible-main-project`
2. `ansible-galaxy install -r roles/requirements_roles.yml`
3. `ansible-playbook playbooks/test_new_test_role.yml -i hosts`

## To install collection and use : 

1. clone in project catalog
2. `cd test-ansible-main-project`
3. `ansible-galaxy install -r requirements_collection.yml`
4. `ansible-playbook playbooks/test_new_collection_with_collections_keyword.yml -i hosts`
   
   `ansible-playbook playbooks/test_new_collection.yml -i hosts`
   
Manual way of install collections
5. `ansible-galaxy collection install git+https://github.com/szymon-m/test-ansible-collection.git,main`
