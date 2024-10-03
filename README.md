# test-ansible-main-project
This is test Ansible main project using Ansible collections


To install collection : (not able to use collection right now)
1. clone in project catalog
2. `cd test-ansible-main-project`
3. `ansible-galaxy collection install git+https://github.com/szymon-m/test-ansible-collection.git,main`


To install and user roles:

1. `cd test-ansible-main-project`
2. `ansible-galaxy install -r roles/requirements_roles.yml`
3. `ansible-playbook playbooks/test_new_test_role.yml -i ../hosts`