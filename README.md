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


## update 2025-02-14

With 2.1.6 of nanokvm: https://github.com/sipeed/NanoKVM/blob/main/CHANGELOG.md#216-6eb4a4e-2025-02-14  
overwrite `/etc/resolv.conf` and make it immutable is not necessary anymore.

`echo "nameserver 192.168.178.1" > /boot/resolv.conf`
