# nanokvm-mitigations

ref: https://youtu.be/plJGZQ35Q6I?si=y-7vLKNhGm4vWOxt


## requirements

ansible


## usage

1. create inventory file

**inv.ini**
```ini
[nanokvm]
192.168.178.63
```

2. **modify cleanup.yml!**
set `ssh_keys: https://github.com/markuman.keys` to your ssh public key


3. run playbook

```
ansible-playbook -i inv.ini cleanup.yml
```
