# TLC Projet

## Camille Croq - Harold Favereau

On peut utiliser l'application web déployée via [ce lien](https://projettlchf.istic.univ-rennes1.fr).

### Diagramme d'architecture

Le diagramme de déploiement ci-dessous représente le diagramme d'architecture des différents conteneurs docker.

![ce fichier](/Diagramme_de_déploiement.png)

Notamment, il n'y a pas de nginx directement sur la VM, le nginx servant de reverse proxy est aussi mis dans un conteneur docker.

### Lancement en local

Pour pouvoir lancer en local, il suffit de lancer la commande

```bash
sudo docker compose -f docker-compose.yml -f docker-compose.local.yml up
```

depuis le racine du projet. On peut alors accéder au front à l'adresse http://localhost/, et à phpmyadmin à l'adresse http://localhost/phpmyadmin/

### Note

Le déploiement sur la VM ne s'est pas fait avec la version actuelle du docker-compose mais avec celle sur [ce tag](https://github.com/ellim4c/doodlestudent/tree/docker-compose-deployment).
