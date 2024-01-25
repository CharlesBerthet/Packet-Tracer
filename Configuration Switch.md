
# Interface VLAN

Paramétrage
```Cisco
>en
#conf t
switch(config)#vlan 10
switch(config-vlan)#ex
switch(config)#int fa0/1
switch(config-if)#switchport mode access
switch(config-if)#switchport access vlan 10

# Ajout d'un autre VLAN
switch(config-if)#switchport access add vlan 20
```

# Interface TRUNK

Paramétrage
```Cisco
>en
#conf t
switch(config)#int fa0/2
switch(config-if)#switchport mode trunk
switch(config-if)#switchport trunk allowed vlan 10

# Ajout d'un autre VLAN
switch(config-if)#switchport trunk allowed vlan add 20
```