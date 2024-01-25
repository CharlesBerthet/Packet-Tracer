
Activer OSPF et associer un ID
```Cisco
router(config)#router ospf <idProcessus>

# Exemple
router(config)#router ospf 11
```

Donner un ID au routeur
```Cisco
router(config-router)#router-id <idRouteur>

# Exemple
router(config-router)#router-id 1.1.1.1
```

Déclarer les réseaux impliqués
```Cisco
router(config-router)#network <adresseIP> <masqueInverse> area <idZone>

# Exemple
router(config-router)#network 192.168.10.0 0.0.0.255 area 11
```

Dispenser une interface
```Cisco
router(config-router)#passive-interface fa0/0
```

Définir la priorité OSPF
```Cisco
router(config-if)#ip ospf priority <valeur-1-à-255>

# Exemple
router(config-if)#ip ospf priority 50
```

Visualiser le voisinage
```Cisco
#show ip ospf neighbor
```

Observer les messages OSPF
```Cisco
#debug ip ospf events
```

Modifier le débit d'une route
```Cisco
router(config-if)#bandwidth 500
```

