PWD := $(shell pwd)
all:
	docker run --rm -e PLUGIN_PLAYBOOK="playbook.yml" -e PLUGIN_INVENTORY="hosts" -e PLUGIN_GALAXY="requirements.yml" -e PLUGIN_REQUIREMENTS="requirements.txt" -e GALAXY_IGNORE_CERTS=true -v $(PWD):$(PWD) -w $(PWD) plugins/ansible
