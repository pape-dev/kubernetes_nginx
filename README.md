TP « Blue/Green » Déploiement :
Ce TP vise à approfondir votre compréhension des déploiements Kubernetes en utilisant
la stratégie de déploiement bleu-vert. Vous allez créer deux déploiements distincts
(bleu et vert) pour une application web, chacun servant une page HTML
personnalisée, et mettre en place un service Kubernetes pour gérer le trafic entre ces
déploiements.
1. Création du déploiement vert (green-deployment.yaml):
o Utilisez l'image Docker nginx.
o Servez une page HTML qui affiche "Hello Green - [Votre Nom et Prénom]".
o Utilisez un ConfigMap pour fournir le contenu HTML personnalisé.
o Configurez des tolerances pour s'assurer que le déploiement peut être exécuté
sur des nœuds avec le rôle control-plane.
o Répliquez l'application (3 réplicas).
2. Création du déploiement bleu (blue-deployment.yaml):
o Utilisez l'image Docker nginx.
o Servez une page HTML qui affiche "Hello Blue - [Votre Nom et Prénom]".
o Comme pour le déploiement vert, utilisez un ConfigMap pour le contenu
HTML personnalisé.
o Ajoutez des tolerances similaires au déploiement vert.
o Répliquez l'application (5 réplicas).
3. Configuration du service Kubernetes (blue-green-service.yaml):
o Créez un service de type LoadBalancer.
o Configurez le service pour qu'il route le trafic initialement vers le déploiement
vert.
