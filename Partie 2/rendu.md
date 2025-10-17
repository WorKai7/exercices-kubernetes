# Rendu TP Virtualisation - Jérôme Vandewalle

## Partie 2

## ----------

Après avoir créé les 4 ressources (Secret, ConfigMap, StatefulSet et Service) pour la base de données mysql, il faut les appliquer :
- ```kubectl apply -f ./database/mysql-secret.yaml -n database```
- ```kubectl apply -f ./database/mysql-configmap.yaml -n database```
- ```kubectl apply -f ./database/mysql-statefulset.yaml -n database```
- ```kubectl apply -f ./database/mysql-service.yaml -n database```

Une fois cela fait, on doit récupérer le nom du pod en cours qui a été créé pour pouvoir entrer dans son terminal après :

- ```kubectl get pods -n database -l app=mysql```

Sortie :

```
NAME      READY   STATUS    RESTARTS   AGE
mysql-0   1/1     Running   0          42s
```

Nous avons donc le nom ```mysql-0``` et nous allons l'utiliser pour entrer dans le terminal du pod en question

- ```kubectl exec -n database -it mysql-0 -- bash```

On se retrouve maintenant dans la console du pod avec cette ligne qui nous est présentée :

- ```bash-5.1# ```

Nous allons maintenant vérifier la présence des 4 variables d'environnement créée avec cette commande :

- ```env | grep MYSQL```

Puis nous avons la sortie suivante :

```
MYSQL_MAJOR=innovation
MYSQL_ROOT_PASSWORD=rooooot
MYSQL_PASSWORD=zinzin
MYSQL_USER=jerome
MYSQL_VERSION=9.0.1-1.el9
MYSQL_DATABASE=wordpress
MYSQL_SHELL_VERSION=9.0.1-1.el9
```

Nous voyons bien que nos variables d'environnement sont présentes et bien spécifiées selon ce que nous avons écrit dans les fichiers YAML

![Sortie des commandes de vérification des variables d'environnement](images/capture1.png)