
# Routeur

Définir une route
```Cisco
router(config)#ip route <AdresseIpRéseau> <MasqueRéseau> <IpProchainRouter>

# Exemple
router(config)#no ip route 192.1268.10.0 255.255.255.0 172.17.252.1
```

Définir une route par défaut
```Cisco
router(config)#ip route 0.0.0.0 0.0.0.0 <IpProchainRouter>

# Exemple
router(config)#ip route 0.0.0.0 0.0.0.0 172.17.252.1
```

Enlever une route
```Cisco
router(config)#no ip route <AdresseIpRéseau> <MasqueRéseau> <IpProchainRouter>

# Exemple
router(config)#no ip route 192.1268.10.0 255.255.255.0 172.17.252.1
```

Montrer les routes
```Cisco
#show ip route
```


# Switch MLS

Création de VLAN
```Cisco
switch(config)#ip routing
switch(config)#vlan 10
```

Affectation de la route au VLAN
```Cisco
switch(config)#int vlan 10
switch(config)#no shutdown

switch(config)#ip address <AdresseIp> <MasqueRéseau>
switch(config)#ip route 0.0.0.0 0.0.0.0 <IpProchainRouter>

# Exemple
switch(config)#ip address 192.168.10.254 255.255.255.0
switch(config)#ip route 0.0.0.0 0.0.0.0 172.17.2.254
```

Mise de l'encapsulation sur l'interface
```Cisco
switch(config)#int fa0/1
switch(config-if)#switchport trunk encapsulation dot1q
switch(config-if)#switchport mode trunk
```

Afficher les routes
```Cisco
#show ip route
```