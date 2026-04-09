**SWITCH-0 COMMANDS**
```
Switch>en
Switch#conf t
Switch(config)#hostname SWITCH-0
SWITCH-0(config)#spanning-tree vlan 1
```

**SWITCH-1 COMMANDS**
```
Switch>en
Switch#conf t
Switch(config)#hostname SWITCH-1
SWITCH-1(config)#spanning-tree vlan 1
```

**SWITCH-2 COMMANDS**
```
Switch>en
Switch#conf t
Switch(config)#hostname SWITCH-2
SWITCH-2(config)#spanning-tree vlan 1
```

**SWITCH-3 COMMANDS**
```
Switch>en
Switch#conf t
Switch(config)#hostname SWITCH-3
SWITCH-3(config)#spanning-tree vlan 1

SWITCH-3(config)#spanning-tree vlan 1 priority 4096
SWITCH-3(config)#spanning-tree vlan 1 root primary
```