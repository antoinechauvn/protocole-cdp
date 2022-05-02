# protocole-cdp-lldp
Découverte du protocole CDP et LLDP

Les protocoles CDP et LLDP sont des protocoles de découverte réseau de niveau 2.

* CDP (propriétaire Cisco, activé par défaut sur les routeurs et commutateurs).
* LLDP (standard interopérable, IEEE 802.1ab).
Leur objectif principal est d’échanger des informations entre périphériques intermédiaires qui peuvent s’identifier finement à travers des messages en format “TLVs” (Type-Length-Value).

## Caractéristiques des protocoles de voisinage L2
Les caractéristiques communes des protocoles de voisinage L2 sont les suivantes :
* Uniquement transmis dans des trames (IEEE 802.3 / IEEE 802.2, par exemple).
* Adresses L2 Multicast réservées.
* CDP et LLDP sont disponibles en plusieurs versions.
* Des délais de mise à jour et de durée de vie.
* Informations transportées dans des TLV (Type-Length-Value)

## Caractéristiques de Cisco Discovery Protocol
Le protocole CDP (Cisco Discovery Protocol):
* propriétaire Cisco
* activé par défaut sur les équipements Cisco
* message CDP envoyé toutes les 60 secondes

Quand le protocole CDP est activé, il envoie les informations suivantes sur tous ces ports :

* Device ID : Le hostname de l’équipement
* Entry address(es): Adresses IP présentes sur l’équipemen
* Platform: Le modèle de l’équipement
* Capabilities: Type d’équipement (switch/routeur)
* Interface :Interface physique où est branché cet équipement
* Port ID : Interface physique de l’interconnexion sur l’équipement en question
* Version : Version d’IOS
* Advertisement version: Version du protocole CDP
* VTP Management Domain: Domaine VTP
* Native VLAN :VLAN natif (par défaut, tout port est en mode access et fait partie de ce fameux VLAN)
* Management address : Adresse IP de management


## Caractéristiques de Link Layer Discovery Protocol
Le protocole LLDP (Link Layer Discovery Protocol):
* protocole standardisé IEEE 802.AB
* désactivé par défaut sur les équipements Cisco

LLDP c’est le protocole. Il envoie des trames LLDPDU pour communiquer.
Dans la LLDPDU, nous y trouvons des TLV ( Type – Length – Value ).
Les TLV contiennent les informations ( Chassis ID , Port ID , TTL TLV et bien d’autre )
LLDP-MED ( LLDP – Media End Point ) est une extension du protocole LLDP.

Le LLDP-MED a été créé afin d’obtenir plus d’information sur les équipements terminaux ( PoE, VOIP, etc … )

Le protocole CDP a été créé avant qu’il y ait un protocole normalisé. LLDP s’est énormément inspiré du protocole CDP. Au niveau des lignes de commandes, il suffit de mettre “LLDP” au lieu de “CDP”.

![image](https://user-images.githubusercontent.com/83721477/166209710-5136b7e1-36e4-412d-ae56-23aff97d93f4.png)
