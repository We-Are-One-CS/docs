Dans le projet GitHub de l'application, la branche sur laquelle va se faire le développement est la branche __dev__.

Lorsque l'on souhaite modifier le code de l'application, on doit :
* Créer une __nouvelle__ branche (avec si possible un nom explicite, en rapport avec les modifications qui y seront faites)
* Une fois les modification faites sur cette nouvelle branche, il convient de faire un __commit__ auquel on donnera un titre explicit et une brève description du travail effectué sur la branche
* On effectue ensuite une __pull request__
* Une fois que l'ensemble des développeur c'est assuré de l'absence de conflit entre le nouveaux code et le code qui éxistait déjà, on peut alors __merge__ la nouvelle branche sur la branche __dev__

***Il est fortement déconseillé de modifier directement la branche dev sous peine d'introduire des erreurs dans le code dont on ne peut connaitre l'origine***
