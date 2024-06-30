### Setup Next-VE on Proxmox
1. Import ovf
2. Add Cloudinit, including Credential and Mgmt IP addr
3. Add NICs
4. Manage by Central Manager
5. Activate License

### Import ovf
+ ssh to proxmox, e.g. ssh root@192.168.100.2 or ssh root@192.168.100.3
+ import ovf, e.g. qm importovf 222 /root/f5/images/BigIP-Next/VE-Next/BIG-IP-Next-20.2.0-2.375.1+0.0.43.ovf local-lvm
### Add Cloudinit & NICs
![alt text](image-2.png)
![alt text](image-3.png)

### Manage by Central Manager

### Activate License

https://community.f5.com/kb/technicalarticles/create-f5-big-ip-next-instance-on-proxmox-virtual-environment/326446


