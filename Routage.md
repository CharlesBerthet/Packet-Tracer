# Redistribution OSPF dans RIP

Entrer dans le paramétrage du protocole RIP
```Cisco
router(config)#router rip
```

Déclarer la redistribution des routes OSPF
```Cisco
router(config-router)#redistribute ospf <idProcessusOSPF> metric <métriqueInjectée>

# Exemple
router(config-router)#redistribute ospf 1 metric 3
```

Déclarer la redistribution des routes statiques
```Cisco
router(config-router)#redistribute static metric <métriqueInjectée>

# Exemple
router(config-router)#redistribute static metric 5
```


# Redistribution RIP dans OSPF

Entrer dans le paramétrage du protocole OSPF
```Cisco
router(config)#router ospf <idProcessusOSPF>
```

Déclarer la redistribution des routes RIP
```Cisco
router(config-router)#redistribute rip metric <métriqueInjectée>

# Exemple
router(config-router)#redistribute rip metric 50
```

Faire évoluer la métrique
```Cisco
router(config-router)#redistribute protocole metric-type 1ou2

# Exemple
router(config-router)#redistribute rip metric 50 metric-type 1
```

# Redistribution OSPF dans OSPF

Entrer dans le paramétrage du protocole OSPF
```Cisco
router(config)#router ospf <idProcessusOSPF>
```

Déclarer la redistribution des routes OSPF
```Cisco
router(config-router)#redistribute static metric 3 metric-type 2 subnets
```