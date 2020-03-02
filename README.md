## Atelier Git

Atelier `git` du [Louvain-li-Nux](http://louvainlinux.org).

Plus d'informations sur <https://louvainlinux.org/activites/atelier-git>

## Compiler les slides

À la racine du repository, exécutez: `make`, le nouveau fichier `main.pdf` devrait s'ouvrir à la fin de la compilation, et être accessible dans le dossier `./build_latex`.

Si vous voulez recompiler, il peut être nécessaire d'exécuter `make clean` avant.

Si vous voulez supprimer les fichiers auxiliaires et logs, vous pouvez exécuter `make clean-aux`

Si vous voulez compiler sans ouvrir le pdf, exécutez `make main`, et `make open` si vous voulez juste ouvrir un pdf déjà compilé.

Les options par défaut passées à `latexmk` sont `-pdf -lualatex -cd -silent`, vous pouvez en ajouter en définissant `LATEX_OPT` dans votre environnement ou en passant sa valeur à `make`, par exemple: `make LATEX_OPT=-verbose`.

Vous pouvez aussi ajouter des instructions `bash` à la fin de la commande, en définissant `BASH_POSTPROCESSING` dans votre environnement ou en passant sa valeur à `make`. Les variables spéciales sont accessibles, par exemple pour rediriger l'output complète vers un logfile pour chaque fichier compilé: `make LATEX_OPT=-verbose BASH_POSTPROCESSING=2>&1 1>$(@D)/out.log`, ou encore pour supprimer tous les logs de `latexmk`: `make BASH_POSTPROCESSING=2>/dev/null 1>/dev/null`. Ces instructions sont simplement inséré à la fin de la commande de compilation `latexmk`.

## Contribuer

N'hésitez pas à proposer des améliorations à ces slides (via pull requests) !

## Déployer des changements

*Information destinée aux membre du Louvain-li-Nux*

La version qui est sur `master` est celle qui est publiée sur [GitHub Pages](https://louvainlinux.github.io/atelier-git/build_latex/main.pdf), vers laquelle les liens du [site du Louvain-li-Nux](https://louvainlinux.org) pointent.

## License

La présentation est disponible sous license `CC-BY 4.0`.

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/">
<img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a>
<br />This work is licensed under a
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

