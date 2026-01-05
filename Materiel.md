Matériels utilisés
1. Introduction
Ce document présente l’ensemble des matériels et outils logiciels utilisés pour la conception, la simulation et la validation de l’infrastructure réseau du projet TechSolutions SARL.
L’architecture a été déployée dans un environnement virtualisé afin de reproduire un contexte d’entreprise réel, tout en respectant les contraintes pédagogiques du workshop.
________________________________________
2. Environnement de simulation
2.1 Outils de simulation et virtualisation
•	GNS3
Utilisé pour la conception de la topologie réseau, la configuration des routeurs et la simulation du backbone OSPF.
•	VirtualBox / VMware
Utilisé pour l’hébergement des machines virtuelles (serveurs et postes clients).
•	Packet Tracer (optionnel)
Utilisé à des fins pédagogiques pour certains tests ou validations de concepts.
________________________________________
3. Équipements réseau
3.1 Routeurs
•	Routeurs virtuels (Cisco / IOS-like)
o	Routeur Backbone (nœud principal)
o	Routeur Internet (R-Internet)
o	Routeurs locaux des départements (RZ-1 à RZ-4)
Rôle : - Routage dynamique OSPF - Interconnexion des départements - Mise en œuvre du NAT et du VPN
________________________________________
3.2 Switchs
•	Switchs virtuels Ethernet
Rôle : - Connexion des postes clients et des serveurs au réseau local de chaque département - Segmentation logique des réseaux
________________________________________
4. Machines virtuelles (serveurs)
4.1 Serveur Web – Département Marketing
•	Type : Machine virtuelle Linux
•	Service principal : Serveur Web (HTTP)
•	Rôle : Hébergement du site Internet de l’entreprise
4.2 Serveur Monitoring – Département IT
•	Type : Machine virtuelle Linux
•	Service principal : Supervision réseau et systèmes
•	Rôle : Surveillance de la disponibilité et des performances
4.3 Serveur Base de Données – Département Gestion
•	Type : Machine virtuelle Linux
•	Service principal : Base de données
•	Rôle : Stockage et gestion des données internes
4.4 Serveur NFS – Département Collaboration
•	Type : Machine virtuelle Linux
•	Service principal : Partage de fichiers (NFS)
•	Rôle : Partage de documents entre les employés
________________________________________
5. Postes clients
•	PC clients virtuels (Linux ou Windows)
•	Nombre simulé : jusqu’à 3 postes par département (à titre représentatif)
Rôle : - Représentation des employés - Accès aux services internes et externes
________________________________________
6. Sécurité (rappel)
•	VPN mis en place entre le backbone et les départements afin de sécuriser les communications internes.
Les aspects de sécurité sont volontairement limités au VPN dans le cadre de ce projet.
________________________________________
7. Conclusion
Les matériels et outils utilisés permettent de simuler une infrastructure réseau d’entreprise réaliste, tout en offrant la flexibilité nécessaire à l’expérimentation, à la configuration et à la documentation du projet.
