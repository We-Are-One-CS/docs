
# Base de données

Ce dossier vise à expliquer les principales relations de la base de données; la base de données principale, ses tableaux, la manière dont les données sont stockées ainsi qu'à donner une image globale de notre base de données.

L'application WAO intranet contient différentes bases de données, ces dernière sont implémentées dans le fichier `wao/models.py`

Si l'on souhaite créer une nouvelle base de données, il faudra le faire dans ce fichier.

Pour plus d'information sur les bases de données sur Django, veuillez consulter la [`documentation`](https://docs.djangoproject.com/en/3.0/topics/db/models/) 

## Spécifications

Service : heroku-postgresql

- PLAN : [standard-0](https://devcenter.heroku.com/articles/heroku-postgres-plans)
- Application de facturation : à chaud

- Région : Paris
- Primaire : Oui
- Version : 
- Création : 
- Sauvegardes : 
- Tableaux : 
- Utilisation : 

## Commandes avec Heroku ##

Utilisez le [Heroku CLI](https://devcenter.heroku.com/articles/heroku-command-line) pour accéder aux journaux à partir de la ligne de commande
```bash 
heroku logs --tail --ps postgres --app brasa
```

Pour se connecter à la base de données (OBS : Il est préférable d'utiliser le DataGrip)
```bash 
heroku psql --app brasa
```

Pour racheter les références de la banque
```bash
heroku pg:credentials:url --app brasa
```

Aide pour afficher des informations sur la base de données
```bash
heroku pg --app brasa --help
```

Pour plus d'informations
```bash
heroku help
```

## Fiche technique

Les dataclips sont essentiellement des requêtes SQL qui peuvent être partagées avec des collègues par le biais de Heroku.
Si vous souhaitez faire une demande que vous jugez intéressante à partager avec l'équipe, n'hésitez pas à l'ajouter [ici](https://data.heroku.com/dataclips).


- Pour plus d'informations : [documentation](https://devcenter.heroku.com/articles/dataclips)

## Tableaux
Pour visualiser les tableaux et leurs relations, nous pouvons utiliser le DataGrip et les exporter en format pdf.
Une version est disponible en [pdf](). 

Pour trouver le diagramme des relations, il suffit de se rendre dans le dossier "tables", cliquer avec le bouton droit de la souris et sélectionner "Diagrammes" et "Afficher la visualisation", ou d'utiliser le raccourci "Ctrl+Alt+Shift+U".


## Relations
Dans la théorie des bases de données relationnelles, il existe 3 principaux types de relations :

1. "Un à un (1 - 1)" :
Une ligne d'un champ de table est liée à un seul autre élément de la table.
Par exemple, nous avons les relations "membre" et "utilisateur". Le membre et l'utilisateur doivent être la même personne. Ils représentent alors un seul élément.
2) "Un à plusieurs (1 - n)" : un élément d'un champ dans un tableau peut être lié à plusieurs autres éléments d'un autre tableau.
Par exemple, nous avons des relations "ville" et "pays". Une ville ne peut avoir qu'un seul pays, mais un pays peut avoir plusieurs villes.
3. "Beaucoup à beaucoup (n - n)" : la relation de pluralité est aller-retour. Par exemple, "utilisateur" et "événement". 
Un utilisateur peut avoir plusieurs événements et un événement peut avoir plusieurs utilisateurs.

## Comment stocker les données

Le stockage des données est très important. Nous devons prendre en considération les aspects suivants 
en ajoutant des données à la base de données BRASA :

1) ```Données actuelles``` : toujours traiter des données actuelles.
2) ```Exhaustivité des données``` : les données doivent être complètes, pas de données corrompues ou incomplètes.
3) ```Propreté des données``` : les données doivent être propres, aucune information ne doit s'ajouter à quoi que ce soit.
4) ```Normalisation des données``` : Les données doivent être normalisées. On ne doit pas utiliser la même colonne de la base de données
pour les données qui appartiennent à deux types de formatage différents.
5) ```Cohérence des données``` : les données doivent être cohérentes. D'un point de vue d'homogénéité, de cohérence et de fermeté. 
Il ne faut pas travailler avec des données qui sont brisées ou qui le seront à terme.

Utilisez la commande :
```
Command:     INSERT
Description: create new rows in a table
Syntax:
[ WITH [ RECURSIVE ] with_query [, ...] ]
INSERT INTO table_name [ AS alias ] [ ( column_name [, ...] ) ]
```

Pour plus d'informations :

- Vidéo SQL : [CS50 SQL](https://www.youtube.com/watch?v=u5pDdEKnbKA)

- Cheatsheet SQL et autres informations : [w3schools SQL](https://www.w3schools.com/sql/sql_ref_keywords.asp) 

