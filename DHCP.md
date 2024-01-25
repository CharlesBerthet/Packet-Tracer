
Déclarer pool d'adresses
```Cisco
router(config)#ip dhcp pool <NomPool>

# Exemple
router(config)#ip dhcp pool 11
```

Indiquer la plage d'adresses du pool
```Cisco
router(dhcp-config)#network <AdresseRéseau> <Masque>

# Exemple 
router(dhcp-config)#network 192.168.30.0 255.255.255.0
```

Indiquer l'adresse passerelle
```Cisco
router(dhcp-config)#default-router <IPpasserelle>

# Exemple
router(dhcp-config)#default-router 192.168.30.254
```

Regarder le paramétrage DHCP
```Cisco
#show run
```

Regarder les adresses qui ont été attribuées
```Cisco
#show ip dhcp binding
```

Exclure une adresse IP de la plage
```Cisco
router(config)#ip dhcp excluded-address <AdresseIP>

# Exemple
router(config)#ip dhcp excluded-address 192.168.30.1
```

Exclure une plage d'adresses IP de la plage
```Cisco
router(config)#ip dhcp excluded-address <PremièreIP> <DernièreIP>

# Exemple
router(config)#ip dhcp excluded-address 192.168.30.250 192.168.30.254
```

