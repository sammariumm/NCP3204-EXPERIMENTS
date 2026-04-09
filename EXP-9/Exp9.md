**ROUTER-1 COMMANDS:**
```
Router>en
Router#conf t
Router(config)#hostname ROUTER-1

ROUTER-1(config)#int fa0/0
ROUTER-1(config-if)#ip add 70.0.0.1 255.0.0.0
ROUTER-1(config-if)#no sh
ROUTER-1(config-if)#ex

ROUTER-1(config)#int eth1/0
ROUTER-1(config-if)#ip add 40.0.0.1 255.0.0.0
ROUTER-1(config-if)#no sh
ROUTER-1(config-if)#ex

ROUTER-1(config-if)#int eth1/1
ROUTER-1(config-if)#ip add 50.0.0.1 255.0.0.0
ROUTER-1(config-if)#no sh
ROUTER-1(config-if)#ex

ROUTER-1(config)#int eth1/2
ROUTER-1(config-if)#ip add 60.0.0.1 255.0.0.0
ROUTER-1(config-if)#no sh
ROUTER-1(config-if)#ex

ROUTER-1(config)#int eth1/1
ROUTER-1(config-if)#no sh
ROUTER-1(config-if)#ex
```
---

**ROUTER-2 COMMANDS:**

```
Router>en
Router#conf t
Router(config)#hostname ROUTER-2

ROUTER-2(config)#int eth1/0
ROUTER-2(config-if)#ip add 40.0.0.2 255.0.0.0
ROUTER-2(config-if)#no sh
ROUTER-2(config-if)#ex
ROUTER-2(config)#

ROUTER-2(config)#int eth1/1
ROUTER-2(config-if)#no sh
ROUTER-2(config-if)#ex
```

---

**ROUTER-3 COMMANDS:**

```
Router>en
Router#conf t
Router(config)#hostname ROUTER-3

ROUTER-3(config)#int eth1/0
ROUTER-3(config-if)#ip add 50.0.0.2 255.0.0.0
ROUTER-3(config-if)#no sh
ROUTER-3(config-if)#ex
ROUTER-3(config)#

ROUTER-3(config)#int eth1/1
ROUTER-3(config-if)#no sh
ROUTER-3(config-if)#ex
```

---

**ROUTER-4 COMMANDS:**

```
Router>en
Router#conf t
Router(config)#hostname ROUTER-4

ROUTER-4(config)#int eth1/0
ROUTER-4(config-if)#ip add 60.0.0.2 255.0.0.0
ROUTER-4(config-if)#no sh
ROUTER-4(config-if)#ex
ROUTER-4(config)#

ROUTER-4(config)#int eth1/1
ROUTER-4(config-if)#no sh
ROUTER-4(config-if)#ex
```

---

**RIP COMMANDS:**

```
ROUTER-1(config)#router rip
ROUTER-1(config-router)#version 2
ROUTER-1(config-router)#network 10.0.0.0
ROUTER-1(config-router)#network 20.0.0.0
ROUTER-1(config-router)#network 30.0.0.0
ROUTER-1(config-router)#network 40.0.0.0
ROUTER-1(config-router)#network 50.0.0.0
ROUTER-1(config-router)#network 60.0.0.0
ROUTER-1(config-router)#network 70.0.0.0
ROUTER-1(config-router)#ex

ROUTER-2(config)#router rip
ROUTER-2(config-router)#version 2
ROUTER-2(config-router)#network 10.0.0.0
ROUTER-2(config-router)#network 20.0.0.0
ROUTER-2(config-router)#network 30.0.0.0
ROUTER-2(config-router)#network 40.0.0.0
ROUTER-2(config-router)#ex

ROUTER-3(config)#router rip
ROUTER-3(config-router)#version 2
ROUTER-3(config-router)#network 10.0.0.0
ROUTER-3(config-router)#network 20.0.0.0
ROUTER-3(config-router)#network 30.0.0.0
ROUTER-3(config-router)#network 50.0.0.0
ROUTER-3(config-router)#ex

ROUTER-4(config)#router rip
ROUTER-4(config-router)#version 2
ROUTER-4(config-router)#network 10.0.0.0
ROUTER-4(config-router)#network 20.0.0.0
ROUTER-4(config-router)#network 30.0.0.0
ROUTER-4(config-router)#network 60.0.0.0
ROUTER-4(config-router)#ex
```

---

**SWITCH COMMANDS (VLAN):**

1. SWITCH 0
    ```
	Switch>en
	Switch#conf t
	Switch(config)#hostname SWITCH-0
	   
	SWITCH-0(config)#vlan 10
	SWITCH-0(config-vlan)#vlan 20
	SWITCH-0(config-vlan)#vlan 30
	SWITCH-0(config-vlan)#ex

	SWITCH-0(config)#int range fa0/1-3
	SWITCH-0(config-if-range)#switchport mode trunk
	SWITCH-0(config-if-range)#ex
	SWITCH-0(config)#

	SWITCH-0(config)#int range fa0/4-6
	SWITCH-0(config-if-range)#switchport mode access
	SWITCH-0(config-if-range)#ex
	   
	SWITCH-0(config)#int fa0/4
	SWITCH-0(config-if)#switchport access vlan 10
	SWITCH-0(config-if)#ex
	   
	SWITCH-0(config)#int fa0/5
	SWITCH-0(config-if)#switchport access vlan 20
	SWITCH-0(config-if)#ex
	   
	SWITCH-0(config)#int fa0/6
	SWITCH-0(config-if)#switchport access vlan 30
	SWITCH-0(config-if)#ex
	```
2. SWITCH 1
    ```
	Switch>en
	Switch#conf t
	Switch(config)#hostname SWITCH-1
	SWITCH-1(config)#vlan 10
	SWITCH-1(config-vlan)#vlan 20
	SWITCH-1(config-vlan)#vlan 30
	SWITCH-1(config-vlan)#ex

	SWITCH-1(config)#int range fa0/1-5
	SWITCH-1(config-if-range)#switchport mode trunk
	SWITCH-1(config-if-range)#ex

	SWITCH-1(config)#int range fa0/6-8
	SWITCH-1(config-if-range)#switchport mode access
	SWITCH-1(config-if-range)#ex
	  
	SWITCH-1(config)#int fa0/6
	SWITCH-1(config-if)#switchport access vlan 20
	SWITCH-1(config-if)#ex
	  
	SWITCH-1(config)#int fa0/7
	SWITCH-1(config-if)#switchport access vlan 30
	SWITCH-1(config-if)#ex
	  
	SWITCH-1(config)#int fa0/8
	SWITCH-1(config-if)#switchport access vlan 10
	SWITCH-1(config-if)#ex
    ```
3. SWITCH 2
    ```
	Switch>en
	Switch#conf t
	Switch(config)#hostname SWITCH-2
	SWITCH-2(config)#vlan 10
	SWITCH-2(config-vlan)#vlan 20
	SWITCH-2(config-vlan)#vlan 30
	SWITCH-2(config-vlan)#EX
	SWITCH-2(config)#

	SWITCH-2(config)#int range fa0/1-3
	SWITCH-2(config-if-range)#switchport mode trunk
	SWITCH-2(config-if-range)#ex

	SWITCH-2(config)#int range fa0/4-6
	SWITCH-2(config-if-range)#switchport mode access
	SWITCH-2(config-if-range)#ex
	  
	SWITCH-2(config)#int fa0/4
	SWITCH-2(config-if)#switchport access vlan 10
	SWITCH-2(config-if)#ex
	  
	SWITCH-2(config)#int fa0/5
	SWITCH-2(config-if)#switchport access vlan 20
	SWITCH-2(config-if)#ex
	  
	SWITCH-2(config)#int fa0/6
	SWITCH-2(config-if)#switchport access vlan 30
	SWITCH-2(config-if)#ex
    ```

**VLAN SETUP:**
1. ROUTER-2
    ```
	ROUTER-2(config)#int eth1/1.10
	ROUTER-2(config-subif)#encapsulation dot1q 10
	ROUTER-2(config-subif)#ip add 10.0.0.1 255.0.0.0
	ROUTER-2(config-subif)#no sh
	ROUTER-2(config-subif)#ex
	  
	ROUTER-2(config)#int eth1/1.20
	ROUTER-2(config-subif)#encapsulation dot1q 20
	ROUTER-2(config-subif)#ip add 20.0.0.1 255.0.0.0
	ROUTER-2(config-subif)#no sh
	ROUTER-2(config-subif)#ex
	  
	ROUTER-2(config)#int eth1/1.30
	ROUTER-2(config-subif)#encapsulation dot1q 30
	ROUTER-2(config-subif)#ip add 30.0.0.1 255.0.0.0
	ROUTER-2(config-subif)#no sh
	ROUTER-2(config-subif)#ex
    ```
2. ROUTER-3
    ```
	ROUTER-3(config)#int eth1/1.10
	ROUTER-3(config-subif)#encapsulation dot1q 10
	ROUTER-3(config-subif)#ip add 10.0.0.2 255.0.0.0
	ROUTER-3(config-subif)#no sh
	ROUTER-3(config-subif)#ex
	  
	ROUTER-3(config)#int eth1/1.20
	ROUTER-3(config-subif)#encapsulation dot1q 20
	ROUTER-3(config-subif)#ip add 20.0.0.2 255.0.0.0
	ROUTER-3(config-subif)#no sh
	ROUTER-3(config-subif)#ex
	  
	ROUTER-3(config)#int eth1/1.30
	ROUTER-3(config-subif)#encapsulation dot1q 30
	ROUTER-3(config-subif)#ip add 30.0.0.2 255.0.0.0
	ROUTER-3(config-subif)#no sh
	ROUTER-3(config-subif)#ex
    ```
3. ROUTER-4
    ```
	ROUTER-4(config)#int eth1/1.10
	ROUTER-4(config-subif)#encapsulation dot1q 10
	ROUTER-4(config-subif)#ip add 10.0.0.3 255.0.0.0
	ROUTER-4(config-subif)#no sh
	ROUTER-4(config-subif)#ex
	  
	ROUTER-4(config)#int eth1/1.20
	ROUTER-4(config-subif)#encapsulation dot1q 20
	ROUTER-4(config-subif)#ip add 20.0.0.3 255.0.0.0
	ROUTER-4(config-subif)#no sh
	ROUTER-4(config-subif)#ex
	
	ROUTER-4(config)#int eth1/1.30
	ROUTER-4(config-subif)#encapsulation dot1q 30
	ROUTER-4(config-subif)#ip add 30.0.0.3 255.0.0.0
	ROUTER-4(config-subif)#no sh
	ROUTER-4(config-subif)#ex
    ```
---
**HRSP CONFIGURATION**

1. ROUTER-2
    ```
	ROUTER-2(config)#int eth1/1.10
	ROUTER-2(config-subif)#standby 10 ip 10.0.0.10
	ROUTER-2(config-subif)#standby priority 120
	ROUTER-2(config-subif)#standby preempt
	ROUTER-2(config-subif)#ex

	ROUTER-2(config)#int eth1/1.20
	ROUTER-2(config-subif)#standby 20 ip 20.0.0.10
	ROUTER-2(config-subif)#standby priority 110
	ROUTER-2(config-subif)#ex

	ROUTER-2(config)#int eth1/1.30
	ROUTER-2(config-subif)#standby 30 ip 30.0.0.10
    ```
2. ROUTER-3
	```
	ROUTER-3(config)#int eth1/1.10
	ROUTER-3(config-subif)#standby 10 ip 10.0.0.10
	ROUTER-3(config-subif)#ex
	
	ROUTER-3(config)#int eth1/1.20
	ROUTER-3(config-subif)#standby 20 ip 20.0.0.10
	ROUTER-3(config-subif)#standby priority 120
	ROUTER-3(config-subif)#standby preempt
	ROUTER-3(config-subif)#ex
	
	ROUTER-3(config)#int eth1/1.30
	ROUTER-3(config-subif)#standby 30 ip 30.0.0.10
	ROUTER-3(config-subif)#standby priority 110
	ROUTER-3(config-subif)#ex
	```
3. ROUTER-4
    ```
	ROUTER-4(config)#int eth1/1.10
	ROUTER-4(config-subif)#standby 10 ip 10.0.0.10
	ROUTER-4(config-subif)#standby priority 110
	ROUTER-4(config-subif)#ex
	  
	ROUTER-4(config)#int eth1/1.20
	ROUTER-4(config-subif)#standby 20 ip 20.0.0.10
	ROUTER-4(config-subif)#ex
	  
	ROUTER-4(config)#int eth1/1.30
	ROUTER-4(config-subif)#standby 30 ip 30.0.0.10
	ROUTER-4(config-subif)#standby priority 120
	ROUTER-4(config-subif)#standby preempt
    ```
---
**Explanations:**
1. The tracert command is successful because no wires were cut. Additionally, the packet is also able to reach the server due to HRSP, and Dynamic routing (RIP). In this case, the packet can choose any route to reach the server.
2. The tracert command remains successful due to HRSP and Dynamic routing (RIP). The packet just uses a different route in order to reach the server.
