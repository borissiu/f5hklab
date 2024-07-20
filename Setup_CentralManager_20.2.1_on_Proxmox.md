### Setup Central Manager (20.2.1) on Proxmox
1. Import OVF & NIC
2. Run CM setup script via Console
3. CM full installation via GUI
4. Somehow App Migration by UCS failed

### 1. Import OVF & NIC
+ Create VM ID 218
'''
qm importovf 218 BIG-IP-Next-CentralManager-20.2.1-0.3.25.ovf local-lvm
qm set 218 -net0 virtio,bridge=vmbr0
'''
+ Start the VM by using default HW setting

### 2. CM initial setup via Console
+ Logon as admin/admin
  + ![alt text](image-29.png)
+ Run setup script
  + ![alt text](image-30.png)
  + ![alt text](image-31.png)

### 3. CM full setup via GUI
+ Logon as admin/admin
+ Run CM Setup
  + **Make sure both circles become GREEN before** 
  + ![alt text](image-32.png)
  + ![alt text](image-34.png)
  + ![alt text](image-33.png)
  + ![alt text](image-35.png)
  + ![alt text](image-36.png)
  + ![alt text](image-37.png)
+ It may show "Unable to load bootstrap info." but never mind
  + ![alt text](image-38.png)
+ Wait 10+ mins and then logon again 

### 4. Somehow App Migration by UCS failed
+ Migrate a BIG-IP user configuration set (UCS) to BIG-IP Next instances
  + ![alt text](image-39.png)
+ ![alt text](image-40.png)
