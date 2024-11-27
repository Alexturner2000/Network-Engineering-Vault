# Aruba 6200F Cookbook
Tags: [[Cookbook]]


### Adding switch to stack
make sure versions match or the switch is under-versioned
```
vsf member <switch-number>
 type jl727a
 link 1 <top-interface>
 link 2 <bottom-interface>
 exit
vsf renumber-to <switch-number>
```

**VSF details**
```
show vsf
show vsf detail
show vsf member
show vsf topology
```
