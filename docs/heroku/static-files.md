# Fichiers statiques

Heroku ne permet pas de stocker des fichiers statiques (images, css (for the site style), etc) dans 
le système qui éxecute notre application (d'ailleurs, c'est un linux: ``Ubuntu 18.04 LTS``). 

C'est pour ce motif que nous allons utiliser le service S3 d'Amazon AWS. En fait, vous avez juste besoin de créer un ``bucket``
pour stocker des fichiers. Un ``bucket`` est comme un dossier en ligne pour stocker des fichiers. Après, notre application 
a tout le code pour intégrer un bucket avec les services réalisés pour l'application Django.

## Pour plus d'informations:

[Amazon S3](https://aws.amazon.com/s3/)

[Prix - Amazon S3](https://aws.amazon.com/s3/pricing/)

[Amazon AWS](https://aws.amazon.com/)
