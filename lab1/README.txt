1	Pratique réseau  Openstack networworking (neutron)

1.1	Deux réseaux de tenant interconnectés par un router
- créer un security-group (autoriser ssh, http, https et icmp)
- créer un réseau privé net1
- créer un sous-réseau subnet1 192.168.1.0/24 attaché à tenantnet1
- ajouter une instance vm1 à net1
- pinger depuis la machine hôte (ops-mono-node). Interprétation ... ?

- pinger depuis le serveur DHCP (ip netns exec q-dhcp* ping ...)
- se connecter par ssh sur vm1 depuis le serveur DHCP
- créer un réseau privé net2
- créer un sous-réseau subnet2 192.168.2.0/24 attaché à net2
- ajouter une instance vm2 à net2

- ping vm1 depuis vm2

- solution interconnexion ?

./cleanup.sh

1.2	Interconnecter deux sous-réseaux de tenant

- créer un réseau privé net1
- créer un sous-réseau subnet1 192.168.1.0/24 attaché à net1
- créer un sous-réseau subnet2 192.168.2.0/24 attaché à net2
- ajouter des instances vm1 à net1->subnet1 et vm2 à net2->subnet2
- ping vm1 depuis vm2

1.3 Installer l'agent neutron-l3 
- créer un réseau public
- Allouer un floating IP à vm1
- Pinger depuis la machine hôte


1.4  Refaire les precedentes etapes avec les APIs REST

http://developer.openstack.org/api-guide/quick-start/index.html
