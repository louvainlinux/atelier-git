Deuxième exercice: les branches. Enoncé
=======================================

Remarque: Cet exercice est volontairement trop compliqué. En pratique, on ne fait pas autant de branches pour de si petites modifications. N'hésitez jamais à utiliser les commandes `git status`, `git log` et `git log --oneline --decorate --graph --all` pour savoir où vous en êtes.


Vous êtes écrivain. Vous rédigez une merveilleuse histoire, que vous voulez versionnez dans git.

Préparation:
------------

Commencez par créer un dépôt git dans le dossier `repo_git`:
```
$ mkdir atelier-git
$ cd atleier-git
$ mkdir ex1
$ cd ex1
$ mkdir repo_git
$ cd repo_git
$ git init
```

Première étape (échauffement):
-----------------------------

Vous avez déjà rédigé les deux premiers chapitres.
(Ou vous les rédigez maintenant dans deux fichier texte séparer).
Mais malencontreusement un faute de frappe s'est glisser dans le chapitre 1 ! (ajouter a votre chap 1 " SSSSSS " quelque part dans votre texte ainsi que 2 * "TTTTT" dans le mileux de votre texte).
Ajoutez-les dans git et faites un commit.

Deuxième étape:
---------------

Vous décidez d'ajouter une illustration à votre histoire. Pour cela, créez une branche "illustration", passez sur cette branche, ajoutez le fichier image.png et faites un commit.

Troisième étape:
----------------

Vous revenez sur la branche master pour modifier le deuxième chapitre. Faites quelques modifications dans le fichier `chap2.txt` et enregistrez-le dans git.

Quatrième étape:
---------------

Vous avez oublié d'ajouter la source de votre illustration. Revenez sur la branche "illustration" et versionnez (ajouter) le fichier source.txt.

Vous êtes satisfait des illustrations et voulez les ajouter à la branche principale (master). Pour cela, passer sur la branche master et fusionnez la branche illustration.

Cinquième étape:
----------------

Vous créez une branche pour rédiger le chapitre 3 (nommée chapitre3).
Vous enregistrez ce fichier dans git.

Vous revenez sur master pour relire le premier chapitre, et vous corrigez une faute de frappe (supprimez les SSSSSS). Vous faites un commit.

Ensuite, vous revenez sur la branche chapitre3 pour relire votre chapitre 3. Il s'avère qu'il n'y a rien à faire: vous avez très bien travaillé.
Ce faisant, vous constatez de nouvelles fautes de frappe dans le fichier chap1.txt, vous les corrigez (supprimez les TTTTT dans le fichier (à deux endroits)).

Enfin, vous allez fusionner les modifications: passer sur la branche master et fusionnez la branche chapitre3. Vous avez un petit conflit à résoudre.

Bonus
-----

Les branches chapitre3 et illustration sont maintenant inutiles, vous pouvez les supprimer (regardez l'aide de la commande  `git branch`).

Vous pouvez créer une branche qui pointe directement sur un commit dans l'historique: `git branch nom-de-branche commit-ID`), vous pouvez donc revenir n'importe où dans l'historique.

Si vous voulez voir les différences entre deux branches: utilisez `git diff`.

