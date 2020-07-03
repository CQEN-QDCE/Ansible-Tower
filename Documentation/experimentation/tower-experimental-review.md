# Expérimentation - Ansible Tower

## Objectif

* Démontrer la possibilité d'utiliser la plateforme Ansile Tower sur OpenShift pour configurer et gérer la PAAS.

## Prérequis
* Vous connaissez Ansible.

* Vous avez accès à une installation d'Ansible Tower sur un cluster OpenShift.

* Vous avez des identifiants pour vous connecter.

## Démarche

* [X] Création d'inventaires
* [X] Création de projets
* [X] Gestion des informations d'identification
* [X] Gestion des accès
* [ ] Gestion des autorisations
* [ ] Création de workflow
* [X] Création de tâches planifiées
* [ ] Utilisation en ligne de commande
* [ ] Automatisation de l'installation et de la configuration d'Ansible Tower sur OpenShift

## Résultats

La plateforme Ansible Tower est une solution web qui rend Ansible encore plus facile à utiliser pour les équipes informatiques de toutes sortes. Il est conçu pour être le centre de toutes les tâches d'automatisation.

Tower permet de contrôler l'accès par rôle de qui peut accéder à quoi. L'inventaire peut être géré graphiquement ou synchronisé avec une grande variété de sources provenant du cloud. Il offre la planification de travaux et enregistre leurs exécution. Il s'intègre bien avec LDAP ou KeyCloak et dispose d'une bonne API REST. Des outils en ligne de commande sont également disponibles pour une intégration facile avec d'autres processus.

### Création d'inventaires
1. Sélectionnez l'option de menu "Inventaires"
2. Ajoutez un inventaire
    * Saisir un nom
    * Saisir une organisation
3. Sélectionnez l'onglet "Hôtes"
4. Ajoutez un hôte
    * Saisir un nom d'hôte, ex: localhost
