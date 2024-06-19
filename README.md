# Node.js-Application
Deployment of Node.js Application on VM with CI/CD using GitHub Actions and Docker Container

## Introduction

Cette documentation décrit le processus étape par étape de déploiement d'une application Node.js sur machine ubuntu en utilisant des conteneurs Docker avec une intégration continue et un déploiement continu (CI/CD) implémentés via GitHub Actions. La pile technologique utilisée comprend Node.js, MongoDB, Docker, GitHub Actions.

## Prérequis

* Un dépôt GitHub contenant le code de votre application Node.js.

* Un compte Docker Hub.
* Les identifiants de la base de données MongoDB.

## Architecture

1. Aperçu des composants :

* Dépôt GitHub
* GitHub Actions
* Docker Hub
* MongoDB Atlas (ou tout autre service d'hébergement MongoDB)

## Étape 1 : Configuration de la VM:
### 1. creation du VM:
* Système d'exploitation : choisissez un système d'exploitation basé sur Linux. J'utilise Ubuntu.
* Groupe de sécurité : autorisez le trafic entrant sur les ports 80, 22 et 443.
  ````
  sudo iptables -A INPUT -p tcp --dport 22 -j ACCEPT
  sudo iptables -A INPUT -p tcp --dport 80 -j ACCEPT
  sudo iptables -A INPUT -p tcp --dport 443-j ACCEPT
  
  ````

### 2. Installez Docker :
Installez Docker  à l'aide de la commande suivante.

`sudo apt install docker.io -y && sudo systemctl start docker`

![image](https://github.com/JRMARIEM/Node.js-Application/assets/161127704/2a70bb6c-be0c-4148-ae5a-64b9bdb226d5)



### 3. Configuration de l'application d'exécution auto-hébergée en tant que service








