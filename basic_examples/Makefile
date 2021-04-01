PWD := $(shell pwd)
all:
	docker run --rm -e PLUGIN_PLAYBOOK="playbook.yml" -e PLUGIN_INVENTORY="hosts" -e PLUGIN_GALAXY="requirements.yml" -e PLUGIN_REQUIREMENTS="requirements.txt" -e ANSIBLE_GALAXY_IGNORE=true -v $(PWD):$(PWD) -w $(PWD) plugins/ansible
test:
	docker run --rm -e ANSIBLE_EXTRA_VARS="clean_up=present" -e ANSIBLE_PYTHON_INTERPRETER=auto_silent -e PLUGIN_PLAYBOOK="create_host_hg.yml" -e PLUGIN_INVENTORY="hosts" -e PLUGIN_GALAXY="requirements.yml" -e PLUGIN_REQUIREMENTS="requirements.txt" -e ANSIBLE_GALAXY_IGNORE=true -v $(PWD):$(PWD) -w $(PWD) plugins/ansible
checkmode:
	docker run --rm -e CHECK=True -e ANSIBLE_EXTRA_VARS="clean_up=present array_ip=192.168.1.30 user=admin password=P@ssw0rd1" -e ANSIBLE_PYTHON_INTERPRETER=auto_silent -e PLUGIN_PLAYBOOK="volume.yml" -e PLUGIN_INVENTORY="hosts" -e PLUGIN_GALAXY="requirements.yml" -e PLUGIN_REQUIREMENTS="requirements.txt" -e ANSIBLE_GALAXY_IGNORE=true -v $(PWD):$(PWD) -w $(PWD) plugins/ansible
