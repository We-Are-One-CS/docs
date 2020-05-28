# Deploy
Le déploiement de l'application weareone et toutes les activités qui rendent le web service disponible pour une utilisation.

Les phases d'activité de déploiement sont:

1. `Libération`: il s’agit parfois de déterminer les ressources nécessaires pour que le système fonctionne avec un rendement et une planification tolérables et/ou documenter les activités subséquentes du processus de déploiement. Donc, il faut savoir la taille des apps qui seront définies avec Heroku.

2. ``Installation et activation``: C'est fait avec Heroku. On push la branche `local/production` (qui doit être testée) comme `heroku/master`.

3. ``Désactivation``: La pratique consistant à retirer des systèmes rarement utilisés ou obsolètes du service est souvent appelée retraite de demande ou déclassement des demandes. Pas besoin dans notre cas.

4. ``Désinstallation``: C’est la suppression d’un système qui n’est plus nécessaire. On n'en a pas besoin dans notre cas.

5. ``Mettre à jour``: Il se compose généralement de désactivation suivie d’installation. Il faut un développeur pour maintenir les nouvelles versions de Django et Python.

6. ``Mise à jour intégrée``: Windows update ou équivalent. Ce n'est pas applicable dans notre cas.

7. ``Suivi de la version``: Realisé dans ``requirements.txt``.

## Django deployment checklist

Avant de deployer l'application, il faut savoir si elle est bonne pour être utilisée dans la vraie vie avec des personnes de We Are One. 

Pour cela, il faut exécuter la commande:

````shell
python manage.py check --deploy
````

Cette commande va vérifier la stabilité de l'application. Nous avons bien réglé des problèmes, mais si vous ajoutez une autre fonctionnalité, il faut penser à le faire.

Pour plus d'informations concernant la Django checklist (on recommande fortement la lecture):

[Django Checklist for deploy link](https://docs.djangoproject.com/en/3.0/howto/deployment/checklist/)

## Production check

La ``production check`` est une feature de Heroku pour savoir si votre application est bien deployée.

Les points à vérifier sont:

1. Heroku-18 Stack
2. Dynos type (on recommande des dynos payés vu leur utilisation)
3. Échec de la redondance des bancs à rouleaux
4. Base de données des Postgres de Production Échoués
5. Haute disponibilité de Postgres
6. Surveillance de l'application en cas d'échec
7. Surveillance du journal des défaillances
8. Pages de maintenance personnalisées
9. Heroku SSL

Pour le serveur en production, on recommande d'avoir des réglages bien gérés.

## Deployment avec heroku

Pour avoir plus d'informations sur le deployment avec Heroku, le lien vers la documentation est:

[Deployment - Heroku](https://devcenter.heroku.com/categories/deployment)

## Préparation d’une base de code pour le déploiement d’Heroku

[Préparation d’une base de code pour le déploiement d’Heroku](https://devcenter.heroku.com/articles/preparing-a-codebase-for-heroku-deployment)
