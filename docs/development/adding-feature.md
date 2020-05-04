### Pour créer une nouvelle fonctionnalité vous devez :

* Créer une url correspondant à la page dédiée à votre fonctionnalité dans le fichier [`wao/urls.py`](https://docs.djangoproject.com/en/3.0/topics/http/urls/)
* Créer le fichier html correspondant à votre nouvelle page dans le dossier [`wao/templates/wao`](https://developer.mozilla.org/fr/docs/Web/HTML)
* Créer les requêtes ayant un lien avec votre nouvelle page dans le fichier [`wao/views.py`](https://docs.djangoproject.com/en/3.0/topics/http/views/)
* Si votre fonctionnalité nécessite un formulaire, vous devez le créer dans le fichier[`wao/forms.py`](https://docs.djangoproject.com/en/3.0/ref/forms/)
* Pour modifier l'apparence de votre page vous devez créer un fichier css corespondant à votre page dans le dossier [`wao/static/wao/css`](https://developer.mozilla.org/fr/docs/Web/CSS/Reference)
* Si vous souhaitez ajouter des images et des polices pour votre page, ceci se fera dans le dossier `wao/static/wao`
