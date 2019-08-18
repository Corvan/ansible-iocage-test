Ansible iocage test
====================
This Project is used to test the 
[ansible iocage module](https://github.com/Corvan/ansible/blob/features/iocage/lib/ansible/modules/system/iocage.py)

The most interesting file to see how the module is used for testing is
[roles/app_ansible_test/tasks/iocage.yml](roles/app_ansible_test/tasks/iocage.yml)

Vagrant
--------
Because not everybody has got a FreeBSd at hand, this project comes
with a vagrant box definition file based on VirtualBox. Go to 
[the vagrant website](https://www.vagrantup.com/) and 
download vagrant; install it afterwards

Setup
------
1. Clone this repository
    `git clone https://github.com/Corvan/ansible-iocage-test`
2. cd into the repo
    `cd ansible-iocage-test`
3. Create a python3 virtualenv
    `python3 -m venv venv`
4. Activate virtualenv
    `source venv/bin/activate`
5. Install requirements
    `pip3 install -r requirements.txt`
6. create vagrant box
    `vagrant up`

Run Ansible playbook
--------------------
Run the tests by running the ansible playbook
`ansible-playbook -i inventory/hosts.yml pb_ansible_test.yml`

Path
------
If you want to look at the iocage ansible module you'll find that inside the venv
under:
`venv/lib/python3.7/site-packages/ansible/modules/system/iocage.py`

Contributing to the module
---------------------------
`git clone https://github.com/Corvan/ansible`

`git checkout features/iocage`
You'll find the module under
`lib/modules/system/iocage.py`