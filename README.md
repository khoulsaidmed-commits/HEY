KAMK — Système de Gestion de Location de Véhicules 

# Description du projet
KAMK est une application web complète dédiée à la gestion intégrale d'une agence de location de véhicules dans le contexte djiboutien. Elle couvre l'ensemble du cycle de vie d'une location : de la réservation en ligne jusqu'à la clôture du contrat, en passant par la facturation kilométrique automatique, la gestion de la flotte et la maintenance des véhicules.
Le projet est né d'un constat terrain : la majorité des agences de location à Djibouti fonctionnent encore sans outil numérique dédié. KAMK apporte une réponse concrète, simple et adaptée aux réalités locales.

 # Objectifs

Digitaliser l'intégralité du cycle de location (réservation, contrat, facturation)
Automatiser le calcul des montants selon la formule : (prix/jour × durée) + frais de livraison − remise
Gérer la flotte en temps réel avec trois statuts : LIBRE, LOUÉ, EN MAINTENANCE
Intégrer un chatbot intelligent basé sur le modèle LLaMA via l'API Groq
Fournir un tableau de bord de pilotage complet à l'administrateur
Garantir la traçabilité juridique complète de chaque contrat


# Présentation de l'équipe
Rôle Membre 
Chef de projet: Abdikarim Souleiman 
Analyste : Kouloud Said
Architecte Kadar AbdirachidTesteur
DocumentationMarwo Osman

Encadrant : [MOUBAREK BARRE]


# Technologies utilisées
Technologie Rôle HTML5 / CSS3 Structure et mise en forme des interfaces JavaScript Dynamisme côté client (AJAX, validation, calculs)PHPLogique métier côté serveur (architecture MVC)MySQLBase de données relationnelle (kamk_bd — 18 tables)WAMP / Apache Environnement de développement et serveur webAPI Groq (LLaMA)Intelligence artificielle pour le chatbot StarUML Modélisation des 7 diagrammes UMLDraw.ioSchémas d'architecture et WBS Gantt Project Planification et suivi du projetGit / GitHub Versionnement du code source

# Fonctionnalités

Côté Client

Création de compte et authentification sécurisée
Consultation du catalogue de véhicules avec disponibilité en temps réel
Réservation en ligne avec calcul automatique du montant
Réservation depuis l'aéroport sans compte préalable
Paiement de l'acompte (carte bancaire ou paiement mobile)
Suivi et consultation des contrats et factures
Convertisseur de devises intégré (USD / EUR / DJF)
Chatbot intelligent disponible 24h/24 pour répondre aux questions

Côté Administrateur / Employé

Tableau de bord avec indicateurs clés en temps réel
Gestion complète de la flotte (ajout, modification, statuts)
Validation des réservations et des paiements
Génération automatique des contrats horodatés
Suivi de la maintenance avec alertes automatiques
Gestion des comptes clients et employés
Export des données en PDF


 Structure du projet
kamk/

 dashboard_admin.php       
 dashboard_employe.php    
 dashboard_client.php      


config/
  └── connexion.php         



 modules/
 reservations.php      
 contrats.php          
 paiements.php         
 facturation.php       
 maintenance.php        
 chatbot.php           



 assets/
  css/                  
  js/                   



 kamk_bd.sql               # Script d'import de la base de données (18 tables)

# Tests réalisés
Quatre niveaux de tests ont été conduits pour valider le système :

Tests unitaires — Vérification des fonctions PHP critiques (calcul facture, disponibilité, hachage bcrypt)
Tests d'intégration — Validation des flux complets entre les modules et la base de données
Tests système — Simulation des 8 scénarios d'utilisation principaux sur les 3 profils
Tests de recette — Validation finale par des utilisateurs non techniques

Résultats : 100% des scénarios validés. Temps de réponse moyen < 2 secondes. Chatbot opérationnel en < 3 secondes. Compatible Chrome, Firefox et Edge.

# Licence
Ce projet est réalisé dans un cadre académique. Toute utilisation commerciale sans autorisation préalable des auteurs est interdite.

# Remerciements
Nous tenons à remercier chaleureusement notre professeur encadrant pour sa disponibilité et ses conseils tout au long de ce projet. Nos remerciements vont également aux professionnels du secteur de la location de véhicules à Djibouti qui ont accepté de partager leur expérience lors de notre phase d'analyse terrain, ainsi qu'à nos familles pour leur soutien constant.

KAMK — Conçu et développé à Djibouti, pour Djibouti. 
