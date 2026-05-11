# Module 1 - Prometheus

## Exercice 1 : Installer Prometheus et accéder à l'interface web

> *Lancer un seul conteneur Prometheus, accéder à l'interface web sur le port 9090 et vérifier que Prometheus se scrape lui-même.*


### 1.1 Récupérer l'image : docker pull prom/prometheus:latest

Pour faire cela, nous lancons `Docker Desktop` puis tapons la commande suivante dans le terminal : `docker pull prom/prometheus:latest`

![alt text](image.png)

---

### 1.2 La lancer : docker run -d --name prometheus -p 9090:9090 prom/prometheus:latest

![alt text](image-1.png)

---

### 1.3 Ouvrir http://localhost:9090 dans votre navigateur

![alt text](image-2.png)

---

### 1.4 Aller dans Status > Targets et confirmer que la cible prometheus est UP

![alt text](image-3.png)

---

## 1.5 Exécuter docker logs prometheus et lire la ligne de démarrage qui annonce le répertoire de stockage

Pour faire ceci, nous tapons `docker logs prometheus` et pouvons voir que lorsque `TSDB` s'initialise, il utilise le répertoire `/prometheus` comme répertoire de stockage.

![alt text](image-4.png)

---

## Exercice 2 : Écrire votre premier prometheus.yml

> *Remplacer la configuration par défaut par votre propre prometheus.yml. Définir un intervalle de scrape global de 10s, un external label environment=lab, et recharger Prometheus sans le redémarrer.*

### 2.1 Arrêter le conteneur précédent : docker rm -f prometheus

Comme énoncé, nous tapons `docker rm -f prometheus`.

![alt text](image-5.png)

Pur vérifier la bonne suppression, nous tapons `docker ps` et pouvons voir que `prometheus` n'est plus affiché, il est donc bien arrêté.

![alt text](image-6.png)

---

### 2.2 



