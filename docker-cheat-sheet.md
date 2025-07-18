# Commandes Docker Essentielles

## Commandes de Base

### Afficher la version de Docker
```bash
docker --version
```

### Informations système Docker
```bash
docker info
```

### Aide générale sur Docker
```bash
docker help
```

---

## Gestion des Images

### Télécharger une image depuis Docker Hub
```bash
docker pull <image>
```

### Lister les images locales
```bash
docker images
```

### Supprimer une image
```bash
docker rmi <image_id>
```

### Construire une image depuis un Dockerfile
```bash
docker build -t <nom>:<tag> .
```

### Ajouter une nouvelle balise à une image
```bash
docker tag <image_id> <repo>:<tag>
```

### Pousser une image vers un registre distant
```bash
docker push <repo>:<tag>
```

---

## Gestion des Conteneurs

### Lancer un conteneur à partir d'une image
```bash
docker run <image>
```

### Lancer un conteneur avec terminal interactif
```bash
docker run -it <image> bash
```

### Lancer un conteneur en arrière-plan (détaché)
```bash
docker run -d <image>
```

### Mappage de ports (local:conteneur)
```bash
docker run -p 8080:80 <image>
```

### Nommer un conteneur au lancement
```bash
docker run --name <nom> <image>
```

### Lister les conteneurs en cours d’exécution
```bash
docker ps
```

### Lister tous les conteneurs (y compris arrêtés)
```bash
docker ps -a
```

### Démarrer un conteneur arrêté
```bash
docker start <id>
```

### Arrêter un conteneur actif
```bash
docker stop <id>
```

### Redémarrer un conteneur
```bash
docker restart <id>
```

### Supprimer un conteneur arrêté
```bash
docker rm <id>
```

### Exécuter une commande dans un conteneur en cours
```bash
docker exec -it <id_ou_nom> bash
```

---

## Volumes et Fichiers

### Créer un volume
```bash
docker volume create <nom>
```

### Lister les volumes
```bash
docker volume ls
```

### Supprimer un volume
```bash
docker volume rm <nom>
```

### Monter un dossier de l'hôte dans un conteneur
```bash
docker run -v <chemin_hote>:<chemin_conteneur> <image>
```

### Copier un fichier du conteneur vers l'hôte
```bash
docker cp <conteneur>:<chemin> <chemin_hote>
```

---

## Réseaux

### Lister les réseaux Docker
```bash
docker network ls
```

### Créer un réseau Docker
```bash
docker network create <nom>
```

### Connecter un conteneur à un réseau
```bash
docker network connect <reseau> <conteneur>
```

---

## Inspection et Maintenance

### Inspecter un conteneur, une image ou un objet
```bash
docker inspect <nom_ou_id>
```

### Voir les logs d'un conteneur
```bash
docker logs <conteneur>
```

### Voir l'utilisation des ressources
```bash
docker stats
```

### Nettoyer les objets Docker inutilisés
```bash
docker system prune
```
