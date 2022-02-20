# Gammoudi_Omar_SRB_2022_docker-

# PROJET DOCKER 

![GitHub-100000_style=for-the-badge logo=github logoColor=white](https://user-images.githubusercontent.com/99410166/154858370-0739f689-ae73-4c57-8d3a-58a7aa6d0506.png)
![Node js-43853D_style=for-the-badge logo=node](https://user-images.githubusercontent.com/99410166/154858418-06e9ea04-3c62-4188-be13-4b9279e39fbe.png)
![MongoDB-4EA94B_style=for-the-badge logo=mongodb logoColor=white](https://user-images.githubusercontent.com/99410166/154858638-e90f7eba-7152-4e31-a813-d2b4c7ccc3e8.png)
![React-20232A_style=for-the-badge logo=react logoColor=61DAFB](https://user-images.githubusercontent.com/99410166/154858435-2d98544a-f3c8-41e7-ba7d-d4738a3f7f3f.png)

# Table des matieres
1) Intro
2) Docker-compose.yml
3) Dockerfile ( Backend )
4) Dockerfile ( Frontend )
5) Descriptif de quelques commandes 




# 1- Intro

- Pour commencer,
    Tout d'abord afin de mener à bien notre projet nous allons creer un docker-compose.yml que nous allons mettre à la racine du github, par la suite 1 Dockerfile sera creer         pour la partie Backend et la partie frontend du projet et quelques commandes pour pouvoir lancer, supprimer copier vos images.


# 2- Docker-compose.yml

Dans notre programme nous utiliserons la version 3 du docker 

3 services seront dans notre docker compose :
  1) web
  2) api
  3) Mango

Pour le premier service on " Build " l'image present dans le frontend en mettant ``build: ./frontend`` 

Ensuite le service web dependra de l'api et cela graçe à la commande ``depends_on``, 

le port qu'on utilisera sera le 3000 qui est le port par defaut de react js 

Par la suite les 2 autres services seront contruits pratiquement de la même façon, 

L'api dependra de mango et on mettra le port par defaut web qui est le 8080.

Pour Mango et on utilisera la commande ``restart: always`` afin de relancer le service à chaque automatiquement.

# 3- Dockerfile ( backend ) 

1:  "From" permet de choisir l'image de base que nous voulons "build"

1: "WORKDIR" permet de définir le répertoire de travail d'un conteneur Docker.

2: "COPY" Elle permet de copier un fichier ou un répertoire local de la machine qui crée l'image Docker dans l'image Docker.

3: "RUN" éxécute les commandes

5: "EXPOSE" expose un port particulier, nous devons mettre le même port dans le docker compose

6: "CMD" crée une valeur par défaut

# 4- Dockerfile (frontend )

1:  "From" permet de choisir l'image que nous voulons "build"

1: "WORKDIR" permet de définir le répertoire de travail d'un conteneur Docker.

2: "ENV" est la definition de variables d'environnement

3: "COPY" Elle permet de copier un fichier ou un répertoire local de la machine qui crée l'image Docker dans l'image Docker.

5: "RUN" éxécute les commandes

6: "EXPOSE" expose un port particulier, nous devons mettre le même port dans le docker compose

7: "CMD" crée une valeur par défaut

# 5- Descriptif de quelques commandes

Apres avoir finis votre Docker compose, votre Dockerfile pour les deux parties nous allons voir quelques commandes pratiques à la bonne utilisation de votre docker 

``Docker-compose up`` il permet de lancer votre docker tout en le demarrant, vous pouvez utilisez aussi ``Docker-compose up -d`` pour qu'il le fasse en arriere plan.

``Docker run`` pour instancier un nouveau conteneur

``docker pull`` pour récupérer une image

``docker build`` pour construire une nouvelle image

``docker image ls" liste tout les image creer

``docker image rm "id" -f`` permet de forcer la suppression du image




