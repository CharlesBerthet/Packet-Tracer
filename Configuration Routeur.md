
# Interface Classique

Paramétrage
```Cisco
>en
#conf t
router(config)#int fa0/2
router(config-if)#no shutdown
router(config-if)#ip address <AdresseIp> <MasqueRéseau>

# Exemple
router(config-if)#ip address 172.17.252.1 255.255.255.252
```

# Interface VLAN

Paramétrage
```Cisco
>en
#conf t
router(config)#int fa0/1
router(config-if)#no shutdown
router(config-if)#no ip address
router(config-if)#ex
router(config)#int fa0/1.10
router(config-if)#encapsulation dot1q 10
router(config-if)#ip address <AdresseIp> <MasqueRéseau>

# Exemple
router(config-if)#ip address 192.168.10.254 255.255.255.0
```
