# RAMANAMBELO NOMERY Mahery Andrew LA-n163-docker

## Feuille de triche des commandes Docker

---

### Commandes de base
* `docker --version`
    Affiche la version de Docker installée.
* `docker info`
    Donne des informations détaillées sur le système Docker.
* `docker help`
    Affiche l'aide générale pour les commandes Docker.

---

### Images
* `docker pull <image>`
    Télécharge une image depuis Docker Hub.
* `docker images`
    Liste les images disponibles localement.
* `docker rmi <image_id>`
    Supprime une image spécifique.
* `docker build -t <nom>:<tag> .`
    Construit une image à partir d'un Dockerfile dans le répertoire courant.
* `docker tag <image_id> <repo>:<tag>`
    Crée une nouvelle balise pour une image.
* `docker push <repo>:<tag>`
    Envoie une image vers un registre distant.

---

### Conteneurs
* `docker run <image>`
    Lance un conteneur à partir d'une image.
* `docker run -it <image> bash`
    Lance un conteneur en mode interactif avec un terminal (shell).
* `docker run -d <image>`
    Lance un conteneur en arrière-plan (mode "detached").
* `docker run -p 8080:80 <image>`
    Mappe le port local `8080` au port `80` du conteneur.
* `docker run --name <nom> <image>`
    Nomme le conteneur lors de son lancement.
* `docker ps`
    Liste les conteneurs en cours d'exécution.
* `docker ps -a`
    Liste tous les conteneurs, y compris ceux qui sont arrêtés.
* `docker start <id>`
    Démarre un conteneur qui a été arrêté.
* `docker stop <id>`
    Arrête un conteneur en cours d'exécution.
* `docker restart <id>`
    Redémarre un conteneur.
* `docker rm <id>`
    Supprime un conteneur arrêté.
* `docker exec -it <id_ou_nom> bash`
    Exécute une commande (ici `bash`) dans un conteneur déjà en cours d'exécution.

---

### Volumes et fichiers
* `docker volume create <nom>`
    Crée un volume Docker.
* `docker volume ls`
    Liste tous les volumes Docker.
* `docker volume rm <nom>`
    Supprime un volume.
* `docker run -v <chemin_hote>:<chemin_conteneur> <image>`
    Monte un dossier de l'hôte dans le conteneur.
* `docker cp <conteneur>:<chemin> <chemin_hote>`
    Copie un fichier ou un dossier du conteneur vers la machine hôte.

---

### Réseaux
* `docker network ls`
    Liste tous les réseaux Docker.
* `docker network create <nom>`
    Crée un nouveau réseau.
* `docker network connect <reseau> <conteneur>`
    Connecte un conteneur à un réseau.

---

### Divers
* `docker inspect <nom_ou_id>`
    Affiche des informations détaillées sur un conteneur, une image, ou un autre objet Docker.
* `docker logs <conteneur>`
    Affiche les journaux (logs) d'un conteneur.
* `docker stats`
    Affiche l'utilisation des ressources (CPU, mémoire, I/O) des conteneurs en cours d'exécution.
* `docker system prune`
    Nettoie les objets Docker inutilisés (conteneurs arrêtés, images orphelines, volumes non attachés).
