# Projet Jenkins avec Docker et Vagrant

Ce projet automatisé vous permet de déployer Jenkins avec Docker dans une machine virtuelle Vagrant. Il utilise Ansible pour la configuration de l'environnement, Docker pour le conteneur Jenkins, et Vagrant pour la gestion de la machine virtuelle.

## Prérequis

Assurez-vous que les éléments suivants sont installés sur votre machine de développement :

- [Vagrant](https://www.vagrantup.com/)
- [VirtualBox](https://www.virtualbox.org/)
- [Git](https://git-scm.com/)

## Installation

1. Clonez ce dépôt Git sur votre machine locale :
   
Exécutez la commande Vagrant pour démarrer la machine virtuelle et provisionner Jenkins avec Docker :

vagrant up
![vagrant-up](https://github.com/youngerdiarrandiaye/jenkins_docker_vagrant/assets/122989242/792781fb-ad23-4fc6-ba1e-792d223d62ce)
![finish instal](https://github.com/youngerdiarrandiaye/jenkins_docker_vagrant/assets/122989242/33c41795-8a56-4693-986c-b2017b61d1f3)

Docker est active vagrant ssh
![docker test](https://github.com/youngerdiarrandiaye/jenkins_docker_vagrant/assets/122989242/302d1765-91ba-40f3-a2af-e3e2ca29b2c5)

Connectez-vous à la machine virtuelle Vagrant :
![connexion sur ma mahine](https://github.com/youngerdiarrandiaye/jenkins_docker_vagrant/assets/122989242/849cf77a-c324-42a9-8260-4c1449297546)
![disponible jenkins](https://github.com/youngerdiarrandiaye/jenkins_docker_vagrant/assets/122989242/8841f682-0e21-4675-9509-90763bbc2664)

Access Jenkins from your browser using the IP address obtained in the previous step:
http://ip-address:8080
Pour obtenir le mot de passe initial de Jenkins, utilisez la commande suivante à l'intérieur de la machine virtuelle 
docker exec $(docker ps -a | grep jenkins | awk '{print $1}') bash -c 'cat /var/jenkins_home/secrets/initialAdminPassword'
![connexion jenkins](https://github.com/youngerdiarrandiaye/jenkins_docker_vagrant/assets/122989242/aa7772f5-3055-40ba-9238-53cdea10449a)

![connexion reuissi](https://github.com/youngerdiarrandiaye/jenkins_docker_vagrant/assets/122989242/a312d16c-11d3-48ee-a37e-0c8d4c92699e)

Creation des pipeline avec mon compte github
lien du projet testé et les fichiers d'installations :
https://github.com/youngerdiarrandiaye/jenkins_docker_vagrant.git
https://github.com/youngerdiarrandiaye/e-banking-spring-backend.git

![pipeline tste](https://github.com/youngerdiarrandiaye/jenkins_docker_vagrant/assets/122989242/1aee4307-dde9-4bfa-9f08-603487d733e3)
![test pip](https://github.com/youngerdiarrandiaye/jenkins_docker_vagrant/assets/122989242/44a03d61-754c-4b40-9bb8-db6579e41258)
