# weareone-intranet app 
[Dashboard - Heroku](https://dashboard.heroku.com)

Le lien pour une application sur Heroku est ``https://dashboard.heroku.com/apps/{weareone-intranet}``, où on a mis le nom
de l'app entre ``{}``. Le vrai  URL n'a pas ces symboles et compte avec le nom de l'app. 

## Overview
Dans cette partie, vous allez avoir les informatinos générales de l'app. Des dynos, les add-ons (avec postgres), activité des collaborateurs,
qui sont les développers responsables pour maintenir l'app. Et finalement, l'histoire des deploys, où on peut voir si jamais 
l'app a changé.

## Resources
Dans resources, vous allez voir un résumé des micro services qui sont en train d'être executés
et comme ça, vous allez voir le prix qui devrait être payé à chaque mois.

## Deploy
Dans deploy, vous avez toutes les informations pour réaliser les deploiements.
En fait, vous avez des options pour réaliser les deploiements. Soit un ``git push``, soit des deploys automatiques avec l'integration `GitHub`.
Toujours, vous pouvez utiliser [`Heroku CLI`: Heroku command line interface](https://devcenter.heroku.com/articles/heroku-command-line) pour aider avec vos deploiements.

## Metrics
Si vous voulez ajouter des métriques pour l'app, c'est par ici. 
C'est une bonne façon de voir comment les utisateurs utilisent la plateforme.

## Activity
Un historique de toutes les activités et tous les déploiements.

## Access
Ici, vous allez voir les personnes qui ont des droits pour changer l'application et réaliser d'autres deploiements.

## Settings
C'est la partie pour réaliser les réglages de l'application. N'hésitez pas à venir ici et changer ce que vous voulez.
En fait, les parties importantes, sont:
- App information: pour changer le nom de l'app
- Config Vars: pour gérer les variables d'environment
- Buildpacks: scripts qui seront éxecutés
- SSL Certificates: certificat pour le https
- Domains: ajouter un domaine (pas herokuapp.com)
- Maintenance mode: Utilisé une fois que vous voulez changer quelque chose dans le site


Pour plus d'informations:
[Dashboard - Heroku](https://dashboard.heroku.com)
