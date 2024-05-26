# student-list 
This repo is a simple application to list student with a webserver (PHP) and API (Flask)

![project](https://user-images.githubusercontent.com/18481009/84582395-ba230b00-adeb-11ea-9453-22ed1be7e268.jpg)


------------


## Application
J'ai déployer une application nommée "student_list", très basique, qui permet à l'entreprise POZOS d'afficher la liste de certains étudiants avec leur âge.

L'application student_list comporte deux modules :

- Le premier module est une API REST (nécessitant une authentification de base) qui envoie la liste souhaitée des étudiants basée sur un fichier JSON
- Le deuxième module est une application web écrite en HTML + PHP qui permet à l'utilisateur final d'obtenir une liste d'étudiants

## Besoin
Mon travail consistait à :

- construire un conteneur pour chaque module
- les faire interagir entre eux
- fournir un registre privé

## Role des fichiers 
Dans mon livrable, vous trouverez trois fichiers principaux : un Dockerfile, un docker-compose.yml et un docker-compose.registry.yml

- `docker-compose.yml` : pour lancer l'application (API et application web)
- `docker-compose.registry.yml` : pour lancer le registre local et son interface utilisateur
- `simple_api/student_age.py` : contient le code source de l'API en python
- `simple_api/Dockerfile `: pour construire l'image de l'API avec le code source à l'intérieur
- `simple_api/student_age.json` : contient le nom et l'âge des étudiants au format JSON
- `index.php` : page PHP où l'utilisateur final se connectera pour interagir avec le service et lister les étudiants avec leur âge.