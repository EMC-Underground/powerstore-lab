# powerstore-lab

### basic_examples
This folder contains simple playbook examples to do the follow:
- Create and Delete a Volume
- Create and Delete a Host
- Create and Delete a Host Group
- Create and Delete a Volume Group
- Create a Volume Snapshot

### Example of How to run a playbook:
```
ansible-playbook volume.yml --extra-vars"array_ip=<array_ip_here> user=admin password=<password_here>"
```

