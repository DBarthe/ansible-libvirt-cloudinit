# ansible-libvirt-cloudinit

Need a specific and undocumented setup.

```ini
[vm:vars]
ansible_host=172.16.91.2
ssh_pub_keys=['your pub key']
memory=4096
cpu=4

[vm]
vm1 ip_suffix=40
vm2 ip_suffix=41
vm3 ip_suffix=42
```

```bash
ansible-playbook playbook.yml
```
```bash
for i in 40 41 42; do ssh centos@172.16.91.$i; done
```
