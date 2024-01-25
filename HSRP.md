
Activer HSRP sur l'interface
```Cisco
router(config)#interface fa0/0
router(config-if)#standby <numGroupe> ip <Ipvirtuelle>

# Exemple
router(config-if)#standby 1 ip 192.168.1.254
```

Donner une priorité HSRP 
```Cisco
router(config-if)#standby <numGroupe> priority <valeur-1-à-255>

# Exemple
router(config-if)#standby 1 priority 150
```

Activer la préemption
```Cisco
router(config-if)#standby <numGroupe> preempt

# Exemple
router(config-if)#standby 1 preempt
```

Modifier les timers Hello et Holdtime
```Cisco
router(config-if)#standby <numGroupe> timers msec <timerHello> msec <timerHoldtime>

# Exemple 
router(config-if)#standby 1 timers msec 200 msec 750
```

Surveiller une autre interface
```Cisco
router(config-if)#standby <numGroupe> track <typeInterface> <numInterface> <réductionDePriorité>

# Exemple
router(config-if)#standby 1 track serial 0/0 20
```

Afficher l'état HSRP 
```Cisco
#show standby brief
```

