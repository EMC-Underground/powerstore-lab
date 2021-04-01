# powerstore-lab

### basic_examples
This folder contains simple playbook examples to do the follow:
- Create and Delete a Volume
- Create and Delete a Host
- Create and Delete a Host Group
- Create and Delete a Volume Group
- Create a Volume Snapshot

### Example of How to run a basic_examples playbook:
```
ansible-playbook volume.yml --extra-vars"array_ip=<array_ip_here> user=admin password=<password_here>"
```

### Examples of how to run the CLI to:
- Create and Delete a Volume
- Create and Delete a Host

```
pstcli -d 10.0.0.1 -u admin -p MyPassword456! -header volume create -name test -size 819200000
```

