# TLC Projet

## Camille Croq - Harold Favereau

On peut utiliser l'application web déployée via [ce lien](https://projettlchf.istic.univ-rennes1.fr).

### Diagramme d'architecture

Le diagramme de déploiement ci-dessous représente le diagramme d'architecture des différents conteneurs docker.

![ce fichier](/Diagramme_de_déploiement.png).

Notamment, il n'y a pas de nginx directement sur la VM, le nginx servant de reverse proxy est aussi mis dans un conteneur docker.
