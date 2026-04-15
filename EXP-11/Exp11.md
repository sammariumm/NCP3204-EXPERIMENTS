# IP Addressing Commands

## DHCP-ROUTER

```
Router>en
Router#conf t
Router(config)#hostname DHCP-ROUTER

DHCP-ROUTER(config)#int se3/0
DHCP-ROUTER(config-if)#ip add 10.0.0.1 255.0.0.0
DHCP-ROUTER(config-if)#no sh
DHCP-ROUTER(config-if)#ex

DHCP-ROUTER(config)#int se2/0
DHCP-ROUTER(config-if)#ip add 30.0.0.1 255.0.0.0
DHCP-ROUTER(config-if)#no sh
DHCP-ROUTER(config-if)#ex
```

## ROUTER-1

```
Router>en
Router#conf t
Router(config)#hostname ROUTER-1
ROUTER-1(config)#int se3/0
ROUTER-1(config-if)#ip add 10.0.0.2 255.0.0.0
ROUTER-1(config-if)#no sh
ROUTER-1(config-if)#ex

ROUTER-1(config)#int se2/0
ROUTER-1(config-if)#ip add 40.0.0.1 255.0.0.0
ROUTER-1(config-if)#no sh
ROUTER-1(config-if)#ex

ROUTER-1(config)#int se6/0
ROUTER-1(config-if)#ip add 20.0.0.1 255.0.0.0
ROUTER-1(config-if)#no sh
ROUTER-1(config-if)#ex
```

## ROUTER-2

```
Router>en
Router#conf t
Router(config)#hostname ROUTER-2

ROUTER-2(config)#int se3/0
ROUTER-2(config-if)#ip add 20.0.0.2 255.0.0.0
ROUTER-2(config-if)#no sh
ROUTER-2(config-if)#ex

ROUTER-2(config)#int se2/0
ROUTER-2(config-if)#ip add 50.0.0.1 255.0.0.0
ROUTER-2(config-if)#no sh
ROUTER-2(config-if)#ex

ROUTER-2(config)#int fa0/0
ROUTER-2(config-if)#ip add 88.1.0.1 255.255.128.0
ROUTER-2(config-if)#no sh
ROUTER-2(config-if)#ex

ROUTER-2(config)#int fa1/0
ROUTER-2(config-if)#ip add 88.1.128.17 255.255.255.240
ROUTER-2(config-if)#no sh
ROUTER-2(config-if)#ex

ROUTER-2(config)#int fa7/0
ROUTER-2(config-if)#ip add 88.0.0.1 255.255.0.0
ROUTER-2(config-if)#no sh
ROUTER-2(config-if)#ex

ROUTER-2(config)#int fa8/0
ROUTER-2(config-if)#ip add 88.1.128.1 255.255.255.240
ROUTER-2(config-if)#no sh
ROUTER-2(config-if)#ex
```

## ROUTER-3

```
Router>en
Router#conf t
Router(config)#hostname ROUTER-3
ROUTER-3(config)#int se2/0
ROUTER-3(config-if)#ip add 30.0.0.2 255.0.0.0
ROUTER-3(config-if)#no sh
ROUTER-3(config-if)#ex

ROUTER-3(config)#int se6/0
ROUTER-3(config-if)#ip add 60.0.0.1 255.0.0.0
ROUTER-3(config-if)#no sh
ROUTER-3(config-if)#ex

ROUTER-3(config)#int se3/0
ROUTER-3(config-if)#ip add 80.0.0.1 255.0.0.0
ROUTER-3(config-if)#no sh
ROUTER-3(config-if)#ex
```

## ROUTER-RA

```
Router>en
Router#conf t
Router(config)#hostname ROUTER-RA
ROUTER-RA(config)#int se7/0
ROUTER-RA(config-if)#ip add 60.0.0.2 255.0.0.0
ROUTER-RA(config-if)#no sh
ROUTER-RA(config-if)#ex

ROUTER-RA(config)#int se2/0
ROUTER-RA(config-if)#ip add 40.0.0.2 255.0.0.0
ROUTER-RA(config-if)#no sh
ROUTER-RA(config-if)#ex

ROUTER-RA(config)#int se6/0
ROUTER-RA(config-if)#ip add 70.0.0.1 255.0.0.0
ROUTER-RA(config-if)#no sh
ROUTER-RA(config-if)#ex

ROUTER-RA(config)#int se3/0
ROUTER-RA(config-if)#ip add 90.0.0.1 255.0.0.0
ROUTER-RA(config-if)#no sh
ROUTER-RA(config-if)#ex
```

## ROUTER-5

```
Router>en
Router#conf t
Router(config)#hostname ROUTER-5
ROUTER-5(config)#int se2/0
ROUTER-5(config-if)#ip add 50.0.0.2 255.0.0.0
ROUTER-5(config-if)#no sh
ROUTER-5(config-if)#ex

ROUTER-5(config)#int se6/0
ROUTER-5(config-if)#ip add 70.0.0.2 255.0.0.0
ROUTER-5(config-if)#no sh
ROUTER-5(config-if)#ex
ROUTER-5(config)#int se3/0

ROUTER-5(config-if)#ip add 100.0.0.1 255.0.0.0
ROUTER-5(config-if)#no sh
ROUTER-5(config-if)#ex
```

## ROUTER-9

```
Router>en
Router#conf t
Router(config)#hostname ROUTER-9
ROUTER-9(config)#int se2/0
ROUTER-9(config-if)#ip add 80.0.0.2 255.0.0.0
ROUTER-9(config-if)#no sh
ROUTER-9(config-if)#ex

ROUTER-9(config)#int se3/0
ROUTER-9(config-if)#ip add 110.0.0.1 255.0.0.0
ROUTER-9(config-if)#no sh
ROUTER-9(config-if)#ex
```

## ROUTER-10

```
Router>en
Router#conf t
Router(config)#hostname ROUTER-10
ROUTER-10(config)#int se3/0
ROUTER-10(config-if)#ip add 110.0.0.2 255.0.0.0
ROUTER-10(config-if)#no sh
ROUTER-10(config-if)#ex

ROUTER-10(config)#int se2/0
ROUTER-10(config-if)#ip add 90.0.0.2 255.0.0.0
ROUTER-10(config-if)#no sh
ROUTER-10(config-if)#ex

ROUTER-10(config)#int se6/0
ROUTER-10(config-if)#ip add 120.0.0.1 255.0.0.0
ROUTER-10(config-if)#no sh
ROUTER-10(config-if)#ex
```

## ROUTER-11

```
Router>en
Router#conf t
Router(config)#hostname ROUTER-11
ROUTER-11(config)#int se3/0
ROUTER-11(config-if)#ip add 120.0.0.2 255.0.0.0
ROUTER-11(config-if)#no sh
ROUTER-11(config-if)#ex

ROUTER-11(config)#int se2/0
ROUTER-11(config-if)#ip add 100.0.0.2 255.0.0.0
ROUTER-11(config-if)#no sh
ROUTER-11(config-if)#ex

ROUTER-11(config)#int fa0/0
ROUTER-11(config-if)#ip add 123.123.123.123 255.128.0.0
ROUTER-11(config-if)#no sh
ROUTER-11(config-if)#ex

ROUTER-11(config)#int fa1/0
ROUTER-11(config-if)#ip add 27.18.30.23 255.128.0.0
ROUTER-11(config-if)#no sh
ROUTER-11(config-if)#ex
```

# DHCP COMMANDS

```
DHCP-ROUTER(config)#ip dhcp pool Network123
DHCP-ROUTER(dhcp-config)#network 123.0.0.0 255.128.0.0
DHCP-ROUTER(dhcp-config)#default-router 123.123.123.123
DHCP-ROUTER(dhcp-config)#dns-server 8.8.8.8
DHCP-ROUTER(dhcp-config)#exit

DHCP-ROUTER(config)#ip dhcp pool Network27
DHCP-ROUTER(dhcp-config)#network 27.0.0.0 255.128.0.0
DHCP-ROUTER(dhcp-config)#default-router 27.18.30.23
DHCP-ROUTER(dhcp-config)#dns-server 8.8.8.8
DHCP-ROUTER(dhcp-config)#exit

DHCP-ROUTER(config)#ip dhcp pool 30k-hosts
DHCP-ROUTER(dhcp-config)#network 88.1.0.0 255.255.128.0
DHCP-ROUTER(dhcp-config)#default-router 88.1.0.1
DHCP-ROUTER(dhcp-config)#dns-server 8.8.8.8
DHCP-ROUTER(dhcp-config)#exit

DHCP-ROUTER(config)#ip dhcp pool 7-hosts
DHCP-ROUTER(dhcp-config)#network 88.1.128.16 255.255.255.240
DHCP-ROUTER(dhcp-config)#default-router 88.1.128.17
DHCP-ROUTER(dhcp-config)#dns-server 8.8.8.8
DHCP-ROUTER(dhcp-config)#exit

DHCP-ROUTER(config)#ip dhcp pool 60k-hosts
DHCP-ROUTER(dhcp-config)#network 88.0.0.0 255.255.0.0
DHCP-ROUTER(dhcp-config)#default-router 88.0.0.1
DHCP-ROUTER(dhcp-config)#dns-server 8.8.8.8
DHCP-ROUTER(dhcp-config)#exit

DHCP-ROUTER(config)#ip dhcp pool 12-hosts
DHCP-ROUTER(dhcp-config)#network 88.1.128.0 255.255.255.240
DHCP-ROUTER(dhcp-config)#default-router 88.1.128.1
DHCP-ROUTER(dhcp-config)#dns-server 8.8.8.8
DHCP-ROUTER(dhcp-config)#exit
```

## ROUTER-2

```
ROUTER-2(config)#int fa0/0
ROUTER-2(config-if)#ip helper-address 10.0.0.1
ROUTER-2(config-if)#ex

ROUTER-2(config)#int fa1/0
ROUTER-2(config-if)#ip helper-address 10.0.0.1
ROUTER-2(config-if)#ex

ROUTER-2(config)#int fa7/0
ROUTER-2(config-if)#ip helper-address 10.0.0.1
ROUTER-2(config-if)#ex

ROUTER-2(config)#int fa8/0
ROUTER-2(config-if)#ip helper-address 10.0.0.1
ROUTER-2(config-if)#ex
```

## ROUTER-11

```
ROUTER-11(config)#int fa1/0
ROUTER-11(config-if)#ip helper-address 10.0.0.1
ROUTER-11(config-if)#ex

ROUTER-11(config)#int fa0/0
ROUTER-11(config-if)#ip helper-address 10.0.0.1
ROUTER-11(config-if)#ex
```

# OSPF COMMANDS

## DHCP-ROUTER

```
DHCP-ROUTER(config)#router ospf 1
DHCP-ROUTER(config-router)#network 10.0.0.0 0.255.255.255 area 0
DHCP-ROUTER(config-router)#network 30.0.0.0 0.255.255.255 area 0
DHCP-ROUTER(config-router)#ex
```

## ROUTER-1

```
ROUTER-1(config)#router ospf 1
ROUTER-1(config-router)#network 10.0.0.0 0.255.255.255 area 0
ROUTER-1(config-router)#network 20.0.0.0 0.255.255.255 area 0
ROUTER-1(config-router)#network 40.0.0.0 0.255.255.255 area 0
ROUTER-1(config-router)#ex
```

## ROUTER-2

```
ROUTER-2(config)#router ospf 1
ROUTER-2(config-router)#network 20.0.0.0 0.255.255.255 area 0
ROUTER-2(config-router)#network 50.0.0.0 0.255.255.255 area 0
ROUTER-2(config-router)#network 88.0.0.0 0.255.255.255 area 0
ROUTER-2(config-router)#ex
```

## ROUTER-3

```
ROUTER-3(config)#router ospf 1
ROUTER-3(config-router)#network 30.0.0.0 0.255.255.255 area 0
ROUTER-3(config-router)#network 60.0.0.0 0.255.255.255 area 0
ROUTER-3(config-router)#network 80.0.0.0 0.255.255.255 area 0
ROUTER-3(config-router)#ex
```

## ROUTER-RA

```
ROUTER-RA(config)#router ospf 1
ROUTER-RA(config-router)#network 40.0.0.0 0.255.255.255 area 0
ROUTER-RA(config-router)#network 70.0.0.0 0.255.255.255 area 0
ROUTER-RA(config-router)#network 60.0.0.0 0.255.255.255 area 0
ROUTER-RA(config-router)#network 90.0.0.0 0.255.255.255 area 0
ROUTER-RA(config-router)#ex
```

## ROUTER-5

```
ROUTER-5(config)#router ospf 1
ROUTER-5(config-router)#network 50.0.0.0 0.255.255.255 area 0
ROUTER-5(config-router)#network 100.0.0.0 0.255.255.255 area 0
ROUTER-5(config-router)#network 70.0.0.0 0.255.255.255 area 0
ROUTER-5(config-router)#ex
```

## ROUTER-9

```
ROUTER-9(config)#router ospf 1
ROUTER-9(config-router)#network 80.0.0.0 0.255.255.255 area 0
ROUTER-9(config-router)#network 110.0.0.0 0.255.255.255 area 0
ROUTER-9(config-router)#ex
```

## ROUTER-10

```
ROUTER-10(config)#router ospf 1
ROUTER-10(config-router)#network 90.0.0.0 0.255.255.255 area 0
ROUTER-10(config-router)#network 110.0.0.0 0.255.255.255 area 0
ROUTER-10(config-router)#network 120.0.0.0 0.255.255.255 area 0
ROUTER-10(config-router)#ex
```

## ROUTER-11

```
ROUTER-11(config)#router ospf 1
ROUTER-11(config-router)#network 100.0.0.0 0.255.255.255 area 0
ROUTER-11(config-router)#network 120.0.0.0 0.255.255.255 area 0
ROUTER-11(config-router)#network 123.0.0.0 0.255.255.255 area 0
ROUTER-11(config-router)#network 27.0.0.0 0.255.255.255 area 0
ROUTER-11(config-router)#ex
```