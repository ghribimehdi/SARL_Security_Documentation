Cahier des charges
Projet : Conception et déploiement d’une infrastructure réseau distribuée
________________________________________
1. Présentation de l’entreprise
TechSolutions SARL est une entreprise spécialisée dans le développement de solutions numériques. Elle s’appuie sur plusieurs départements fonctionnels afin d’assurer ses activités : - Web / Marketing - Supervision / IT - Gestion / Base de données - Partage / Collaboration interne - Securite
Dans un contexte de croissance et de professionnalisation, l’entreprise souhaite moderniser son infrastructure informatique afin de répondre aux exigences actuelles de disponibilité, de sécurité et d’évolutivité.
________________________________________
2. Contexte et objectifs du projet
2.1 Contexte
Le projet s’inscrit dans un cadre pédagogique sous forme de workshop. Il vise à simuler un environnement réseau d’entreprise réel à l’aide d’outils de virtualisation et de simulation réseau (GNS3, Packet Tracer, VirtualBox).
Chaque étudiant représente un rôle réseau ou un département spécifique. L’architecture repose sur un nœud principal (backbone) assurant l’interconnexion de l’ensemble des départements.
2.2 Objectifs principaux
•	Garantir la disponibilité des services critiques pour les employés et les clients.
•	Assurer une sécurité renforcée du réseau et une hiérarchisation efficace des flux.
•	Mettre en place une supervision proactive pour anticiper et corriger les incidents.
•	Concevoir une architecture évolutive, modulaire et conforme aux standards professionnels.
________________________________________
3. Périmètre du projet
3.1 Inclus dans le projet
•	Conception d’une topologie réseau multi-zones.
•	Mise en place d’un backbone OSPF.
•	Segmentation du réseau via VLSM.
•	Déploiement de services sur machines virtuelles.
•	Mise en œuvre des mécanismes de sécurité (VPN, NAT).
•	Documentation complète du projet.
3.2 Hors périmètre
•	Déploiement sur infrastructure physique réelle.
•	Haute disponibilité avancée (cluster, load balancing réel).
•	Sécurité applicative approfondie.
________________________________________
4. Description générale de l’architecture réseau
4.1 Backbone (cœur du réseau)
Le backbone représente le cœur de l’infrastructure réseau de TechSolutions SARL. Il assure l’interconnexion de l’ensemble des départements et garantit la circulation fiable et sécurisée des flux internes.
•	Constitué de N + 1 routeurs, où N correspond au nombre de départements/services.
•	Topologie maillée, permettant une redondance logique et une meilleure tolérance aux pannes.
•	Utilisation du protocole de routage dynamique OSPF, assurant une convergence rapide et une gestion hiérarchisée des routes.
•	Un routeur du backbone est désigné comme nœud principal, jouant le rôle de point central d’interconnexion et de coordination.
Le backbone constitue également le point d’intégration des mécanismes de sécurité globaux et de l’accès Internet.
4.2 Accès Internet
•	Routeur principal R-Internet, connecté au backbone.
•	Simulation de l’accès Internet via la mise en œuvre de NAT/PAT.
•	Séparation claire entre réseau interne et réseau externe.
________________________________________
5. Plan d’adressage IP
•	Plage allouée par le fournisseur : 10.10.0.0/15
•	Segmentation du réseau via VLSM afin d’optimiser l’utilisation des adresses IP.
•	Chaque département dispose de son propre sous-réseau adapté au nombre d’hôtes requis.
________________________________________
6. Départements et services
6.1 Département Sécurité (transversal)
Le département Sécurité n’est pas une zone utilisateur classique, mais un rôle transversal intégré principalement au backbone.
Il est chargé de : - La définition et l’application des politiques de sécurité réseau. - La mise en œuvre des VPN site-à-site ou client-serveur entre le backbone et les départements. - Le contrôle et la hiérarchisation des flux inter-départements. - La sécurisation de l’accès Internet via NAT et règles de filtrage.
Ce département s’appuie sur les équipements du backbone et sur le routeur Internet pour garantir la confidentialité, l’intégrité et la disponibilité des communications.
6.1 Web / Marketing
•	Routeur local : RZ-1
•	Service VM : Serveur Web
•	Nombre théorique de clients : 6810 PCs
•	Rôle : Gestion du site Internet et interactions avec les clients externes.
6.2 Supervision / IT
•	Routeur local : RZ-2
•	Service VM : Serveur de monitoring
•	Nombre théorique de clients : 1270 PCs
•	Rôle : Supervision des performances et de la disponibilité des équipements.
6.3 Gestion / Base de données
•	Routeur local : RZ-3
•	Service VM : Serveur Base de Données
•	Nombre théorique de clients : 424 PCs
•	Rôle : Centralisation et sécurisation des données.
6.4 Partage / Collaboration
•	Routeur local : RZ-4
•	Service VM : Serveur NFS
•	Nombre théorique de clients : 192 PCs
•	Rôle : Partage interne de fichiers et documents.
Remarque : Sur la maquette GNS3, un maximum de trois postes clients sera configuré à titre représentatif par zone.
________________________________________
7. Fonctionnalités à implémenter
7.1 Réseau et connectivité
•	Routage dynamique OSPF.
•	Segmentation VLSM.
•	Attribution automatique des adresses IP via DHCP.
•	Vérification de l’accessibilité entre réseaux locaux et distants.
7.2 Services sur machines virtuelles
•	Serveur Web (Marketing).
•	Serveur Base de Données (Gestion).
•	Serveur NFS (Collaboration).
•	Serveur de Monitoring (IT).
7.3 Sécurité
•	VPN site-à-site ou client-serveur entre le backbone et les départements.
•	NAT pour l’accès Internet sécurisé.
•	Contrôle des flux inter-zones.
________________________________________
8. Organisation des rôles
•	Administrateur Backbone / Internet :
o	Configuration OSPF, NAT et VPN.
•	Administrateurs de départements (4) :
o	Configuration des routeurs locaux, PC clients et serveurs VM.
•	Responsable coordination, documentation et sécurité (optionnel) :
o	Supervision globale du projet.
o	Rédaction de la documentation.
o	Vérification de la cohérence et des mesures de sécurité.
________________________________________
9. Déroulement du projet
Chaque séance du workshop comprend : - Une partie théorique (OSPF, VLSM, DHCP, VPN, NAT). - Une mise en pratique sur les outils de simulation.
Un fascicule pédagogique guide les différentes étapes de configuration et de validation.
________________________________________
10. Livrables attendus
•	Topologie réseau fonctionnelle sous GNS3.
•	Configuration des routeurs et services.
•	Documentation technique complète.
•	Captures d’écran justifiant la faisabilité et le bon fonctionnement.
________________________________________
11. Conclusion
Ce projet permet de mettre en œuvre une architecture réseau professionnelle, sécurisée et évolutive, tout en développant des compétences pratiques en conception, configuration, supervision et documentation d’infrastructures réseau d’entreprise.
