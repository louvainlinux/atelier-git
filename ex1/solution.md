Deuxième exercice: les branches. Solution.
=========================================

Première étape (échauffement):
-----------------------------

```
$ git add chap1.txt chap2.txt
$ git commit
```


Deuxième étape:
---------------

```
$ git branch illustration
$ git checkout illustration
$ git add image.png
$ git commit
```

Troisième étape:
----------------

```
$ git checkout master
$ git add chap2.txt
$ git commit
```

Quatrième étape:
---------------

```
$ git checkout illustration
$ git add source.txt
$ git commit
$ git checkout master
$ git merge illustration
```

Cinquième étape:
----------------

```
$ git branch chapitre3
$ git checkout chapitre3
$ git add chap3.txt
$ git commit
$ git checkout master
$ # Edition chap1.txt
$ git add chap1.txt
$ git commit
$ git checkout chapitre3
$ # Edition chap1.txt
$ git add chap1.txt
$ git commit
$ git checkout master
$ git merge chapitre3
$ git status
$ # Edition chap1.txt pour corriger les conflits
$ git add chap1.txt # marque le conflit comme resolu
$ git commit # valide la fusion
```

Bonus
-----

```
$ git branch -d illustration
$ git branch -d chapitre3
$ git log
$ git branch chapitre1 [id de commit]
$ git diff chapitre1 master
```



