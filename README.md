# Cook Openvpn

## Install Ansible on Linux

```
$ sudo apt-add-repository ppa:ansible/ansible
$ sudo apt-get update
$ sudo apt-get install ansible
```

## Install Ansible on OSX

```
$ sudo easy_install pip
$ sudo pip install ansible
```

## Deploy OpenVPN server

Playbook does not create client config files by default
```
$ ansible-playbook site.yml
```

## Generate client certificates

```
$ ansible-playbook site.yml -t client -e "clientname=elon"
```