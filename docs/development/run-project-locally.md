Clonez le projet sur votre PC et changez le répertoire : 
```bash
$ git clone git@github.com:We-Are-One-CS/intranet.git
$ cd intranet/
```

Migrez la base de donnée : 

```bash
$ python manage.py makemigrations wao 

$ python manage.py migrate --noinput
```

lancez l'application sur un server Django : 

```bash
$ python manage.py runserver
```

Maintenant vous devriez voir votre application en tapant http://127.0.0.1:8000 dans votre moteur de recherche. 


Quand vous avez fini, n'oublez pas de quitter le server : 

```bash
Quit the server with CTRL-BREAK
(In Windows) Ctrl + C
```
