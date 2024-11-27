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

