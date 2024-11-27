# Catalyst 3750 Cookbook
Tags: [[Cookbook]], [[Cisco]]

### Unstack a previously used switch
```
configure terminal
switch {stack-member-number} renumber 1
no switch {stack-member-number} provision
write memory
reload
```

### TACACS config (don't paste until live)
```
aaa authentication login default local group tacacs+
aaa authentication enable default group tacacs+ enable
aaa authentication dot1x default group {group}
aaa authorization console
aaa authorization config-commands
aaa authorization exec default group tacacs+ local
aaa authorization commands 0 default group tacacs+ none
aaa authorization commands 1 default group tacacs+ if-authenticated
aaa authorization commands 15 default group tacacs+ if-authenticated
aaa authorization network default group {group}
aaa accounting dot1x default start-stop group {group}
aaa accounting commands 1 default start-stop group tacacs+
aaa accounting commands 15 default start-stop group tacacs+
aaa accounting connection default start-stop group tacacs+
```

### TACACS server config

```
aaa group server tacacs+ {group_name}
 server name {name}
 server name {name}

aaa group server radius {group_name}
 server name {name}
 server name {name}
 
aaa server radius dynamic-author
 client ip server-key {key}
 client ip server-key {key}
 port 3800
```

### Reload
```
reload in {time-in-minutes}
reload cancel
```

### Updating the switch
The 3750 doesn't have any USB ports, thus we must use a file transfer protocol. Either TFTP or SCP. Ensure that switch has enough memory in the flash to boot from the IOS. It is known that some old Cisco 3750v2 have not enough memory and cannot upgrade to a version with SHA256 (aka garbage switch)
1. **Check memory space**
```
show flash
! delete flash:<filename>
```
2. **Configure Network settings**
	Both the PC and the switch will need to be in the same subnet and connected together via ethernet. Here is some basic config
```
interface vlan 1
 ip address 192.168.0.3 255.255.255.0
 no shutdown
 exit

interface fa 1/0/1
 switchport mode access
 switchprot access vlan 1

---

netsh interface show interface
netsh interface ip set address name="Ethernet 2" static 192.168.0.2 255.255.255.0 192.168.0.1
netsh interface ip set address name="Ethernet 2" dhcp

```
3. **Set Up fileserver on PC**
	SolarWinds and MobaXterm have TFTP servers and they work internally
4. **Transfer the image**
```
copy tftp://192.168.0.2/3750-ipservicesk9-tar.122-55.SE11.bin flash:

! to check if its copied ! dir flash: 
```
5. **Change the boot variable**
```
config t
boot system flash:c3750-ipbasek9-mz.150-2.SE11.bin
end
wr mem
reload
```
