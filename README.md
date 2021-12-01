Define hosts IPs in cluster.yaml

Create Vagrant cluster
```
vagrant up
```

Setup Consul and Nomad
```
ansible-playbook -i hosts main.yml -v
```