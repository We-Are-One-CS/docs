# Serveur

Pour gérér le serveur, on récommend que la personne chargé regarde le [tutoriel d'utilisation python avec heroku](https://devcenter.heroku.com/articles/getting-started-with-python), il y a beaucoup 
des notions importantes pour gérér l'application.

## Visualiser les fichiers logs

Heroku traite les journaux (fichiers logs) comme des flux d’événements commandés dans le temps agrégés à partir des flux de sortie de toutes vos applications et des composants Heroku, fournissant un canal unique pour tous les événements.

Affichez des informations sur votre application en cours d’exécution à l’aide d’une des commandes de journalisation, `heroku logs --tail`

## Échelle de l'application

Vous pouvez vérifier combien de dynos sont en cours d’exécution à l’aide de la commande: `ps`

````shell
$ heroku ps
Free dyno hours quota remaining this month: 999h 6m (99%)
Free dyno usage for this app: 0h 0m (0%)
For more information on dyno sleeping and how to upgrade, see:
https://devcenter.heroku.com/articles/dyno-sleeping

=== web (Free): gunicorn gettingstarted.wsgi (1)
web.1: up 2018/10/12 14:26:45 -0500 (~ 33s ago)
````

Par défaut, votre application est déployée sur un dyno gratuit. Les dynos gratuits dormiront après une demi-heure d’inactivité (s’ils ne reçoivent pas de trafic). Cela entraîne un retard de quelques secondes pour la première demande au réveil. Les demandes subséquentes fonctionneront normalement. Les dynos gratuits consomment également à partir d’un quota mensuel de dyno gratuit - tant que le quota n’est pas épuisé, toutes les applications gratuites peuvent continuer à fonctionner.

Pour éviter le sommeil de dyno, vous pouvez passer à un passe-temps ou un type de dyno professionnel tel que décrit dans l’article Dyno Types. Par exemple, si vous migrez votre application vers un dyno professionnel, vous pouvez facilement l’évolur en exécutant une commande indiquant à Heroku d’exécuter un nombre spécifique de dynos, chacun exécutant votre type de processus Web.

L’échelle d’une application sur Heroku équivaut à modifier le nombre de dynos qui sont en cours d’exécution. Échelle du nombre de dynos web à zéro:

````shell
heroku ps:scale web=0
````

Échelle à nouveau:
````shell
heroku ps:scale web=1

````

## Démarrer une console

Vous pouvez exécuter une commande, généralement des scripts et des applications qui font partie de votre application, dans un dyno unique en utilisant la commande. Il peut également être utilisé pour lancer un processus REPL attaché à votre terminal local pour expérimenter dans l’environnement de votre application: `heroku run`

````shell
$ heroku run python manage.py shell
Python 3.7.6 (default, Dec 23 2019, 04:25:22)
[GCC 7.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
(InteractiveConsole)
>>>
````

Si vous recevez une erreur, alors vous devrez peut-être configurer votre pare-feu. ``Error connecting to process``

La coque Python est en cours d’exécution dans le contexte de votre application et toutes ses dépendances. De là, vous pouvez importer certains de vos fichiers d’application.

Pour avoir une idée réelle de la façon dont les dynos fonctionnent, vous pouvez créer un autre dyno unique et exécuter la commande, qui ouvre une coquille sur ce dyno. Vous pouvez ensuite y exécuter des commandes. Chaque dyno a son propre espace de fichier éphémère, peuplé de votre application et de ses dépendances - une fois que la commande terminée (dans ce cas, ), le dyno est supprimé.

````shell
$ heroku run bash
Running `bash` attached to terminal... up, run.3052
~ $ ls
gettingstarted  hello  manage.py  Procfile  README.md  requirements.txt  runtime.txt  staticfiles
~ $ exit
exit
````

N’oubliez pas de taper pour sortir de la coquille et mettre fin au dyno. ``exit``

