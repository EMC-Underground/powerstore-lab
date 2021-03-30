PWD := $(shell pwd)
all:
	docker run --rm -e PLUGIN_PLAYBOOK="playbook.yml" -e PLUGIN_INVENTORY="hosts" -e PLUGIN_GALAXY="requirements.yml" -e PLUGIN_REQUIREMENTS="requirements.txt" -e ANSIBLE_GALAXY_IGNORE=true -v $(PWD):$(PWD) -w $(PWD) plugins/ansible
test:
	docker run --rm -e PLUGIN_PLAYBOOK="create_host_hg.yml" -e PLUGIN_INVENTORY="hosts" -e PLUGIN_GALAXY="requirements.yml" -e PLUGIN_REQUIREMENTS="requirements.txt" -e ANSIBLE_GALAXY_IGNORE=true -v $(PWD):$(PWD) -w $(PWD) plugins/ansible
