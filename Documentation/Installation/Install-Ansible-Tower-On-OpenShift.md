Install-Ansible-Tower-On-OpenShift.md


# Install Ansible Tower on OpenShift

Read this in: [Français](Install-Ansible-Tower-On-OpenShift.fr.md)

## Prerequisites
* You have access to the URL of an OpenShift Web console.

* You have credentials to log in.

* You have an OpenShift CLI (oc) installed and you can connect to the OpenShift cluster from a terminal.

## Procedure
1. Log in to OpenShift Wen Console.

2. Create a new project called "ansible-tower".

3. Add a "Persistent Volume Claims" named "postgresql" with 10 GB of space.

4. Download the latest version of the installer [Ansible Tower OpenShift Setup](https://releases.ansible.com/ansible-tower/setup_openshift/?extIdCarryOver=true&sc_cid=701f2000001OH6fAAG).

5. Extract the contents of the archive.

6. Change the value of the following keys in the "inventory" file
   | Key       | Value     |
   | :--- | :--- |
   |  admin_user | Tower super user name    |
   |  admin_password | Tower super user password    |
   |  secret_key | secret key to encrypt the vault - must be kept carefully between each update    |
   |  pg_username | Postgresql super user name    |
   |  pg_password | Postgresql super user password     |
   |  openshift_host | OpenShift cluster api url    |
   |  openshift_project | ansible-tower    |
   |  openshift_user | OpenShift cluster super user name    |
   |  openshift_password | OpenShift cluster super user passwrod    |
 
7. Execute the script ./setup_openshift.sh

## Liens externes
[Installing Ansible Tower on OpenShift - A Strumble-through by Ken Moini](https://www.youtube.com/watch?v=QHF8HwLl39A)

[Ansible Tower - OpenShift Deployment and Configuration](https://docs.ansible.com/ansible-tower/3.5.0/html/administration/openshift_configuration.html)


