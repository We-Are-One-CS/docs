### Principe de Django

Django est un framework basé sur le principe MVC ou MTV composé de trois parties distinctes :

1. Un langage de gabarits flexible qui permet de générer du HTML, XML ou tout autre format texte ;
2. Un contrôleur fourni sous la forme d'un « remapping » d'URL à base d'expressions rationnelles ;
3. Une API d'accès aux données est automatiquement générée par le cadre compatible CRUD. Inutile d'écrire des requêtes SQL associées à des formulaires, elles sont générées automatiquement par l'ORM.

En plus de l'API d'accès aux données, une interface d'administration fonctionnelle est générée depuis le modèle de données. Un système de validation des données entrées par l'utilisateur est également disponible et permet d'afficher des messages d'erreur automatiques.

Sont également inclus :
* un serveur web léger permettant de développer et tester ses applications en temps réel sans déploiement ;
* un système élaboré de traitement des formulaires muni de widgets permettant d'interagir entre du HTML et une base de données. De nombreuses possibilités de contrôles et de traitements sont fournies ;
* un cadre de cache web pouvant utiliser différentes méthodes (MemCached, système de fichier, base de données, personnalisé) ;
* le support de classes intermédiaires (intergiciel) qui peuvent être placées à des stades variés du traitement des requêtes pour intégrer des traitements particuliers (cache, internationalisation, accès…) ;
* une prise en charge complète d'Unicode.

Pour plus d'informations, consultez [la documentation Django](https://docs.djangoproject.com/en/3.0/)
