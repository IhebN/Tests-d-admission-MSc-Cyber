Exercice 1 – Projet Réseau
1. Présentation du projet
Ce projet consiste à concevoir et configurer un réseau informatique en utilisant Cisco Packet Tracer.
L’objectif est de mettre en place une infrastructure réseau fonctionnelle avec :
•	Plusieurs VLAN
•	Des liaisons trunk
•	Du routage inter-VLAN
•	Un service DHCP
•	Une connexion Wi-Fi via des Access Points
________________________________________
2. Objectifs techniques
Les objectifs principaux de ce projet sont :
•	Segmenter le réseau avec des VLAN
•	Permettre la communication entre les VLAN grâce au routeur
•	Fournir automatiquement des adresses IP avec DHCP
•	Mettre en place l’accès Wi-Fi pour les laptops
•	Vérifier le bon fonctionnement avec des tests de connectivité
________________________________________
3. Topologie du réseau
Le réseau est composé de :
•	1 routeur (Router0)
•	3 switches (Switch3, Switch4, Switch5)
•	Des PC, laptops et téléphones IP
•	Des Access Points pour le Wi-Fi
Les switches sont interconnectés en trunk et le routeur est relié au switch central pour assurer le routage inter-VLAN.
________________________________________
4. Étapes de réalisation
4.1 Câblage
•	Connexion des PC, laptops et téléphones IP aux switches
•	Connexion des switches entre eux
•	Connexion du switch principal au routeur
•	Connexion des Access Points aux switches
________________________________________
4.2 Création des VLAN
VLAN	Nom	Usage
10	WIFI	Réseau Wi-Fi
20	PC_FIXES	Postes fixes
30	ADMIN	Administration
1	Default	VLAN natif
Les VLAN suivants ont été créés :
________________________________________
4.3 Configuration des ports
•	Les ports reliés aux utilisateurs sont configurés en mode access
•	Les ports entre switches et vers le routeur sont configurés en mode trunk
•	Les VLAN 1,10,20,30 sont autorisés sur les trunks
4.4 Configuration du routeur
•	Mise en place du router-on-a-stick
•	Création des sous-interfaces :
o	G0/0.10 → VLAN 10
o	G0/0.20 → VLAN 20
o	G0/0.30 → VLAN 30
•	Attribution des adresses IP passerelles :
o	192.168.10.1
o	192.168.20.1
o	192.168.30.1

4.5 Mise en place du DHCP
•	Création de pools DHCP pour chaque VLAN
•	Attribution automatique des adresses IP
•	Configuration du DNS (8.8.8.8)
________________________________________
4.6 Configuration du Wi-Fi
•	Paramétrage des Access Points
•	Création du SSID
•	Connexion des laptops en Wi-Fi
•	Vérification de l’accès réseau
________________________________________
5. Tests et validation
Les tests suivants ont été réalisés :
•	Ping entre les PC et leur passerelle
•	Ping entre machines de VLAN différents
•	Vérification de l’attribution automatique d’IP
•	Test de connexion Wi-Fi
•	Vérification du routage inter-VLAN

