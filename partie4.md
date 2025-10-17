Jérôme Vandewalle

Question 1: Qu'est-ce qu'un Pod en Kubernetes?
B. Un groupe de conteneurs agissant comme une unité logique

Question 2: Quelle commande est utilisée pour créer un Namespace?
B. kubectl create namespace <nom-du-namespace>

Question 3: Lequel des composants suivants est responsable de la communication avec l'API Server?
A. kubelet

Question 4: Qu'est-ce qu'un ConfigMap dans Kubernetes?
B. Une ressource pour stocker des données de configuration non sensibles

Question 5: Comment exécuter un Job planifié en Kubernetes?
B. En utilisant un CronJob

Question 6: Qu'est-ce qu'un Deployment en Kubernetes?
B. Un contrôleur responsable de la gestion des mises à jour de vos pods

Question 7: Quel composant est responsable de l'équilibrage de charge et du basculement entre les pods dans un Service?
B. kube-proxy

Question 8: Comment afficher les journaux d'un pod particulier en cours d'exécution?
A. kubectl logs <pod-name>

Question 9: Que se passe-t-il lorsqu'un Pod échoue ?
A. Il est recréé par une réplication

Question 10: Quelle est la différence entre ConfigMap et Secret ?
C. Secret est pour des données sensibles

Question 11: Qu'est-ce qu'un Namespace en Kubernetes ?
B. Une méthode de partitionnement du cluster en plusieurs environnements virtuels

Question 12: Comment Kubernetes permet-il de réclamer un volume ?
C. PersistentVolumeClaim

Question 13: Quel est le rôle de l'API Server dans l'architecture de Kubernetes ?
C. Il expose l'API RESTful de Kubernetes et agit en tant que point d'entrée pour toutes les opérations d'administration du cluster.

Question 14: Comment Kubernetes assure-t-il la sécurité et l'isolation des applications dans un cluster partagé?
B. En appliquant le Role-Based Access Control (RBAC), les Pod Security Policies (PSP), et les Network Policies pour gérer les autorisations et l'isolation des pods.

Question 15: Quel est l'impact de la définition incorrecte des "requests" et "limits" des ressources (CPU et mémoire) pour les pods dans un cluster Kubernetes, et comment cette configuration affecte-t-elle le Scheduler et le Quality of Service (QoS) des pods ?
A. Si les "requests" sont trop basses, le Scheduler peut placer trop de pods sur un nœud, entraînant une surallocation, tandis que des "limits" trop élevées peuvent provoquer un throttling intensif des applications.


Bonus: Laquelle des affirmations suivantes n'est pas incorrecte concernant l'usage des ConfigMaps et des Secrets dans un cluster Kubernetes ?
C. Les Secrets sont stockés de manière encodée en base64 dans etcd, mais ils ne sont pas chiffrés par défaut.

