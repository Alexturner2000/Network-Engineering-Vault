# Scripts Cookbook
Tags: [[Cookbook]], [[Code]]

# Turning text to CSV
Example.txt 
```
Accesspoint02  groupname2       505         Down
Accesspoint01  groupname1         205         Up 33d:12h:28m:27s
Accesspoint04  groupname4        505         Down
Accesspoint03  groupname3          205         Up 33d:12h:28m:28s                    
```

1. Remove irregular spaces using regex, and replace with a space
```
 \s{2,}
```
2. Find all spaces (not inside quotations), and replace with commas
```
(?<!")\s(?![^"]*")
```
 

---
# IP Change PowerShell
Terminal as Administrator
```
netsh interface show interface
netsh interface ip set address name="Ethernet 2" static 192.168.0.2 255.255.255.0 192.168.0.1
netsh interface ip set address name="Ethernet" dhcp
```