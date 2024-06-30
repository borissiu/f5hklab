### Setup Next-VE on Proxmox
1. Import **ovf**
2. Add NICs & **Cloudinit Drive** 
3. Start Next-VE and then **Remove Cloudinit Drive**
4. Run setup script
5. Manage by Central Manager
6. Activate License

### Import ovf
+ ssh to proxmox, e.g. ssh root@192.168.100.2 or ssh root@192.168.100.3
+ import ovf, e.g. qm importovf 222 /root/f5/images/BigIP-Next/VE-Next/BIG-IP-Next-20.2.0-2.375.1+0.0.43.ovf local-lvm

### Add NICs & Cloudinit Drive
+ E1000 for mgmt and Virtio for others  
![alt text](image-5.png)
+ Credential, e.g. admin/admin, ip=192.168.100.22/24, gw=192.168.100.1  
![alt text](image-3.png)

### Start Next-VE and then Remove Cloudinit Drive
+ Start Next-VE
+ Remove CloudInit Drive. Otherwise, CLI access may fail in next bootup.

### Run setup script
+ Change admin password, e.g. Welcome123!
![alt text](image-4.png)

+ Check status, e.g. sudo kubectl get pods
![alt text](image-6.png)

### Manage by Central Manager
+ Connect to CM, e.g. https://192.168.100.210  
![alt text](image-8.png)
![alt text](image-9.png)

### Activate License
![alt text](image-10.png)

### Supplementary Info.
+ BIG-IP-Next-20.2.0-2.375.1+0.0.43
  + Ubuntu 22.04.4 TLS  
  + ![alt text](image-7.png)

+ admin account was disable after running setup
  
+ https://community.f5.com/kb/technicalarticles/create-f5-big-ip-next-instance-on-proxmox-virtual-environment/326446



