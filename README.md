# Automatic Splunk Enterpise Installation by fyrworx4

### Reference: https://bussenet.com/index.php/2019/02/09/automating-splunk-universal-forwarder-deployment-with-ansible/

## Description:

This Ansible playbook is used to install a 30-day trial of Splunk Enterprise 8.0.4.


## Folder Directory:

ansible.cfg
hosts
roles/
playbooks/
	splunk_install/
		main.yml
		roles/
			common/
				files/
					splunk-8.0.4.1-ab7a85abaa98-Linux-x86_64.tgz
					user-seed.conf
				tasks/
					main.yml
playbooks

## How to use:

First, run: ansible-vault encrypt /etc/ansible/playbooks/splunk_install/roles/common/files/user-seed.conf and enter in a password.

Then, run: ansible-playbook --ask-become-pass --ask-vault-pass /etc/ansible/playbooks/splunk_install/main.yml