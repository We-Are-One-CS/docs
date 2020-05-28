# Données sur Heroku

[Heroku - Données](https://data.heroku.com/)

On peut penser a une application sur Heroku comme étant une ensemble de micro-services.
C'est-à-dire, il aura le dyno pour l'application web, après il aura l'add-on PostgreSQL pour gérer la base de données
et finalement, si vous voulez ajouter d'autre chose, vous pouvez les ajouter (par exemple, un service de recherche des données, moteur de recherche elastique, etc).

Finalement, pour tout le donnée du deploy, il faut utiliser la partie data de Heroku.

## Dashboard

Ici, on peut voir l'application et ses definitions.
C'est vraiment important de voir les variables d'environment et les laisser toujours secrètes.
Elles ont un rôle important dans le fonctionnement de l'app.

## Data

Ici, il aura une liste de bases de données pour ajouter à l'application avec ses types et beaucoup d'options.

Vous allez avoir l'option de changer la taille de la base, voir la quantité des tableaux disponibles, etc.


## Dataclips

Les dataclips sont des lignes de commande SQL. En fait, ils ont l'objectif de créer, modifier, supprimer des lignes de la base de données.

Pour plus d'informations, allez dans la partie SQL de la documentation.

## Documentation
[Documentation pour heroku](https://devcenter.heroku.com/)

## Pour plus d'informations

[Heroku - Données](https://data.heroku.com/)

[Heroku - Support](https://data.heroku.com/)
