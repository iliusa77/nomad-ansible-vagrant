## Project description
- Launch Vagrant cluster from 3 hosts
- Setup Consul server + 2 Consul clients, Nomad server


### Prerequisites
```
Linux Ubuntu 18.04
Vagrant 2.2.19
Virtualbox 6.1
Ansible 2.11.6
```


### Variables
Define hosts IPs in hosts, cluster.yaml and main.yml

Create Consul key and put in `consul_key` variable in main.yml
```
wget https://releases.hashicorp.com/consul/1.5.0/consul_1.5.0_linux_amd64.zip && \
unzip consul_1.5.0_linux_amd64.zip && \
chmod +x ./consul && \
./consul keygen
Ss89NxNorsdTfupJv22OHQ==
```

### Setup
Create Vagrant cluster, setup Consul and Nomad + demo job
```
vagrant up --provision && ansible-playbook -i hosts main.yml -v
```

Open Consul
```
http://192.168.56.101:8500/ui/dc1/services
```

Open Nomad
```
http://192.168.56.101:4646
```