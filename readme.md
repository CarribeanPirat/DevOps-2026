# Partie 1 — Les bases 🟢

## Exercice 1 — Premier contact avec Docker 

### 1.1 __Téléchargez l'image nginx:alpine depuis Docker Hub sans lancer de conteneur.__

Pour ce faire, nous utilisons Docker Desktop et allons dans l'onglet docker Hub puis, dans la barre de recherche nous tapons `nginx`. Il nous propose plusieurs versions, nous prenons la plus récente.

![alt text](image-3.png)

---

### 1.2 __Lancez un conteneur nginx:alpine nommé mon-nginx en arrière-plan, en exposant le port 8080 de votre machine sur le port 80 du conteneur.__

L'idée ici est de runner le container avec l'image précédente et la nommer "mon-nginx" puis de cliquer sur le bouton `Run`

![alt text](image-4.png)

---

### 1.3 __Vérifiez que le conteneur tourne. Quelle commande permet de lister uniquement les conteneurs en cours d'exécution ?__

On peut trouver facilement la commande qui permet de liser uniquement les ocnteneurs en cours d'exécution. La commande qui permet cela est `docker ps`

![alt text](image-2.png)

---

### 1.4 __Ouvrez `http://localhost:8080` dans votre navigateur (ou avec curl ). Que voyez-vous ?__

Nous pouvons voir une page Nginx prouvant que le conteneur Docker est bien lancé et que le serveur web Nginx fonctionne correctement à l'intérieur.

![alt text](image-1.png)

---

### 1.5 __Affichez les logs du conteneur mon-nginx.__

Les logs sont accessibles en cliquant directement sur le nom du container. 

![alt text](image-5.png)
![alt text](image-6.png)

---

### 1.6 __Arrêtez le conteneur mon-nginx sans le supprimer. Puis listez tous les conteneurs (y compris arrêtés). Quelle est la différence avec la commande de la question 1.3 ?__

Pour arrêter le container, nous tapons dans le terminal `docker stop mon-nginx`. Pour vérifier `TOUS` les containers, y compris ceux qui sont arrêtés, comme la commande suite à la question 1.3, nous pouvons trouver cette dernière rapidement suite à une recherche web. Nous devons ajouter le paramètre `-a` dans la commande. Cela donne `docker ps -a`. 

![alt text](image-8.png)

---

### 1.7 __Supprimez le conteneur mon-nginx . Vérifiez qu'il n'existe plus.__

La commande `docker rm mon-nginx` permet de supprimer le container. On vérifie en tapant la commande vue précédemment : `docker ps -a`. On peut voir qu'aucuns containers ne s'affiche, ce dernier a bien été supprimé.

![alt text](image-9.png)

---

### 1.8 __Quelle commande aurait permis de lancer le conteneur de façon à ce qu'il soit automatiquement supprimé à l'arrêt ?__

La commande qui permet de lancer un container puis qu'il se supprime automatiquement une fois stoppé est : `docker run --rm <image>`

## Exercice 2 — Construire sa première image avec un Dockerfile 


