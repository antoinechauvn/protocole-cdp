# protocole-cdp
Découverte du protocole CDP

On peut trouver des protocoles de voisinage L2, au niveau de la couche Liaison de données :
Utilité : identification, diagnostic, surveillance, gestion et configuration des périphériques.
Protocoles CDP et LLDP.
Vulnérable dans l’environnement L2.
Diagnostic de base : si ces protocoles sont fonctionnels, la couche 2 est donc fonctionnelle.

Deux protocoles de voisinage de couche L2 sont courants :

CDP (propriétaire Cisco, activé par défaut sur les routeurs et commutateurs).
LLDP (standard interopérable, IEEE 802.1ab).
Leur objectif principal est d’échanger des informations entre périphériques intermédiaires qui peuvent s’identifier finement à travers des messages en format “TLVs” (Type-Length-Value).
Caractéristiques des protocoles de voisinage L2
Les caractéristiques communes des protocoles de voisinage L2 sont les suivantes :

Uniquement transmis dans des trames (IEEE 802.3 / IEEE 802.2, par exemple).
Portée L2.
Adresses L2 Multicast réservées.
CDP et LLDP sont disponibles en plusieurs versions.
Des délais de mise à jour et de durée de vie.
Informations transportées dans des TLV (Type-Length-Value)

Caractéristiques de Cisco Discovery Protocol
Les caractéristiques de Cisco Discovery Protocol (CDP) sont les suivantes :

Cisco Discovery Protocol, propriétaire Cisco Systems
Protocole de couche 2 (embarqués dans des trames) :
Adresse de destination 01:00:0c:cc:cc:cc
Logical-Link Control
DSAP: SNAP (0xaa)2
Organization Code: Cisco (0x00000c)
PID: CDP (0x2000)
Mises à jour par défaut toutes les 60 secondes.
Informations retenues (“holdtime”) 3 X 60 secondes = 180 s.
Activé par défaut sur toutes les interfaces
A désactiver (globalement ou par interfaces) car très indiscret
