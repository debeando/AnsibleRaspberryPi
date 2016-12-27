# Ansible for RaspberryPi

## Install

```bash
brew install ansible
```

## Search

How to search ip address for RaspberryPi on our network

```bash
sudo nmap -sP 192.168.1.0/24 | awk '/^Nmap/{ip=$NF}/B8:27:EB/{print ip}'
```

## Deploy

```bash
ansible-playbook -i hosts playbook.yml --sudo
```

## Services

### SSH:

- Password: osmc

```
ssh osmc@osmc.local
```

### Deluge:

- Password: deluge

```
http://osmc.local:8112
```

### Samba:

- User: osmc
- Password: osmc

```
smb://osmc.local
```

### InfluxDB:

```
http://osmc.local:8083
```

### Grafana:

```
http://osmc.local:3000
```
