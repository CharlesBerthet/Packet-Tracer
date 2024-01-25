
Regrouper une plage d'interface physique dans une interface logique
```Cisco
router(config)#interface range fa0/1, fa1/1, fa2/1
router(config-if-range)#channel-group <numGroupe> mode <auto/desirable>

# Exemple
router(config-if-range)#channel-group 1 mode auto
```

Consulter la configuration d'agrégation
```Cisco
#show etherchannel summary
```

