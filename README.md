Define hosts IPs in hosts, cluster.yaml and main.yml

Create Consul key and put in `consul_key` variable in main.yml

Create Vagrant cluster
```
vagrant up
```

Setup Consul and Nomad
```
ansible-playbook -i hosts main.yml -v
```

Open Consul
```
http://192.168.56.101:8500/ui/dc1/services
```

Open Nomad
```

```