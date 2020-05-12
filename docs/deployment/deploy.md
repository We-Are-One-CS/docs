# Deploy
Le déploiement de l'application weareone est toutes les activités qui rendent le web service disponible pour une utilisation.

Les phases d'activité de déploiement sont:

1. `Libération`: il s’agit parfois de déterminer les ressources nécessaires pour que le système fonctionne avec un rendement et une planification tolérables et/ou documenter les activités subséquentes du processus de déploiement. Donc, il faut savoir la taille des apps qui seront définis avec Heroku.

2. ``Installation et activation``: C'est fait avec heroku. On push la branch `local/production` (qui doit être testé) comme `heroku/master`.

3. ``Désactivation``: La pratique consistant à retirer des systèmes rarement utilisés ou obsolètes du service est souvent appelée retraite de demande ou déclassement des demandes. Pas besoin dans notre cas.

4. ``Désinstallation``: C’est la suppression d’un système qui n’est plus nécessaire. Pas besoin dans notre cas.

5. ``Mettre à jour``: Il se compose généralement de désactivation suivie d’installation. Il faut un devélopper pour maintainer les nouvelles versions de Django et python.

6. ``Mise à jour intégrée``: Windows update ou quelque chose comme ça. Pas applicable dans notre cas.

7. ``Suivi de la version``: Realisé dans ``requirements.txt``.

## Django deployment checklist

Avant de deployer l'application, il faut savoir si elle est bonne pour être utilisé dans la vraie vie avec des personnes de We Are One. 

Pour cela, il faut exécuter le command

````shell
python manage.py check --deploy
````

Ce command va vérifier la stabilité de l'application. Nous avons bien reglé des problèmes. Mais si vous ajoutez une autre fonctionnalité, il faut le faire.

Pour plus d'informations concernant le Django checklist (on récommend la lecture fortement):

[Django Checklist for deploy link](https://docs.djangoproject.com/en/3.0/howto/deployment/checklist/)

## Production check

Le ``production check`` est une feature de Heroku pour savoir si votre app est bien deployé ou pas.

Les points sont:

1. Heroku-18 Stack
2. Dynos type (on récommend des dynos payés vu leur utilisation)
3. Échec de la redondance des bancs à rouleaux
4. Base de données des Postgres de Production Échoués
5. Haute disponibilité de Postgres
6. Surveillance de l'application en cas d'échec
7. Surveillance du journal des défaillances
8. Pages de maintenance personnalisées
9. Heroku SSL

Pour le serveur en production, on récommend avoir des réglagés bien gérés.

## Deployment avec heroku

Pour voir plus d'informations sur le deployment avec Heroku, le lien vers la documentation est:

[Deployment - Heroku](https://devcenter.heroku.com/categories/deployment)

## Préparation d’une base de code pour le déploiement d’Heroku

[Préparation d’une base de code pour le déploiement d’Heroku](https://devcenter.heroku.com/articles/preparing-a-codebase-for-heroku-deployment)
