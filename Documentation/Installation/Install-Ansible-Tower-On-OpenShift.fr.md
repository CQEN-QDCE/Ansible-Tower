Install-Ansible-Tower-On-OpenShift.md


# Installer Ansible Tower sur OpenShift

Lisez ceci en: [English](Install-Ansible-Tower-On-OpenShift.md)

## Prérequis
* Vous avez accès à l'URL de la console Web OpenShift.

* Vous avez des identifiants pour vous connecter.

* Vous avez un OpenShift CLI (oc) d'installé et vous pouvez vous connectez au cluster OpenShift à partir d'un terminal.

## Procédure
1. Accédez à la console Web OpenShift.

2. Créez un nouveau projet nommé "ansible-tower".

3. Ajoutez un "Persistent Volume Claims" nommé "postgresql" de 10 Go d'espace.

4. Téléchargez la dernière version de l'installateur [Ansible Tower OpenShift Setup](https://releases.ansible.com/ansible-tower/setup_openshift/?extIdCarryOver=true&sc_cid=701f2000001OH6fAAG).

5. Extraire le contenu de l'archive.

6. Modifiez la valeur des clés suivantes dans le fichier "inventory"
   | Clé       | Valeur     |
   | :--- | :--- |
   |  admin_user | nom du super utilisateur Tower    |
   |  admin_password | mot de passe du super utilisateur Tower    |
   |  secret_key | clé secrète pour chiffrer la voute - dois être conservée précieusement entre chaque mise à jour    |
   |  pg_username | nom du super utilisateur Postgresql    |
   |  pg_password | mot de passe du super utilisateur Postgresql    |
   |  openshift_host | url de l'api du cluster OpenShift    |
   |  openshift_project | ansible-tower    |
   |  openshift_user | nom du super utilisateur du cluster OpenShift    |
   |  openshift_password | mot de passe du super utilisateur du cluster OpenShift   |
 
7. Exécutez le script ./setup_openshift.sh

## Liens externes
[Installing Ansible Tower on OpenShift - A Strumble-through by Ken Moini](https://www.youtube.com/watch?v=QHF8HwLl39A)

[Ansible Tower - OpenShift Deployment and Configuration](https://docs.ansible.com/ansible-tower/3.5.0/html/administration/openshift_configuration.html)


