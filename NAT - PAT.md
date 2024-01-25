
# NAT Statique

Déclarer le NAT sur `l'interface interne` du routeur
```Cisco
router(config-if)#ip nat inside
```

Déclarer le NAT sur `l'interface externe` du routeur
```Cisco
router(config-if)#ip nat outside
```

Saisir les IP de traduction
```Cisco
router(config)#ip nat inside source static <IPprivée> <IPpublique>

# Exemple
router(config)#ip nat inside source static 192.168.0.1 200.1.1.1
```

Afficher la table NAT d'un routeur
```Cisco
#show ip nat translations
```


# NAT Dynamique

Déclarer le NAT sur `l'interface interne` du routeur
```Cisco
router(config-if)#ip nat inside
```

Déclarer le NAT sur `l'interface externe` du routeur
```Cisco
router(config-if)#ip nat outside
```

Déclarer le pool d'adresses IP public
```Cisco
router(config)#ip nat pool NomPool <1èreIP> <DernièreIP> netmask <Masque>

# Exemple
router(config)#ip nat pool POOL_EXEMPLE 200.1.1.1 200.1.1.3 netmask 255.255.255.0
```

Autoriser les IP privées à communiquer
```Cisco
router(config)#access-list <NuméroListe> permit <IPprivée> <MasqueInversé>

# Exemple
router(config)#access-list 20 permit 192.168.10.0 0.0.0.255
```

Associer la liste d'IP privées au pool d'IP public
```Cisco
router(config)#ip nat inside source list <NuméroListe> pool <NomPool>

# Exemple
router(config)#ip nat inside source list 20 pool POOL_EXEMPLE
```


# PAT

Déclarer le NAT sur `l'interface interne` du routeur
```Cisco
router(config-if)#ip nat inside
```

Déclarer le NAT sur `l'interface externe` du routeur
```Cisco
router(config-if)#ip nat outside
```

Déclarer le pool avec une adresse IP public unique
```Cisco
router(config)#ip nat pool NomPool <IPunique> <IPunique> netmask <Masque>

# Exemple
router(config)#ip nat pool POOL_IP 200.1.1.1 200.1.1.1 netmask 255.255.255.0
```

Autoriser les IP privées à communiquer
```Cisco
router(config)#access-list <NuméroListe> permit <IPprivée> <MasqueInversé>

# Exemple
router(config)#access-list 20 permit 192.168.10.0 0.0.0.255
```

Associer la liste d'IP privées à l'adresse IP public
```Cisco
router(config)#ip nat inside source list <NuméroListe> pool <NomPool> overload

# Exemple
router(config)#ip nat inside source 20 NuméroListe pool POOL_IP overload
```

Mapper la liste sur une interface du routeur
```Cisco
router(config)#ip nat inside source list <NuméroListe> interface <NomInterface> overload

# Exemple
router(config)#ip nat inside source list 20 interface g0/0 overload
```

Affecter un port public défini (pour les serveurs)
```Cisco
router(config)#ip nat inside source static tcp <IPprivée> <NuméroPortPrivé> <IPpublique> <NuméroPortPublic>

# Exemple
router(config)#ip nat inside source static tcp 192.168.2.1 80 8.8.8.8 80
```
