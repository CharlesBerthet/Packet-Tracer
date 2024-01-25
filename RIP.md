
Activer le RIP
```Cisco
router(config)#router rip 
router(config-router)#version 2
```

Déclarer chaque réseau voisin
```Cisco
router(config-router)#network <adresseIP>

router(config-router)#network 192.168.1.0
```

Désactivé l'option de résumé (qui est activé par défaut)
```Cisco
router(config-router)#no auto-summary
```

