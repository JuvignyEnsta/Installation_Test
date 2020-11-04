# Installation_Test

Test l'installation des différents outils nécessaires au cours IN203

## Comment exécuter le test ?

Si vous avez installé MSYS 2, éditer le fichier "Makefile" et commenter la première ligne :

    include Make.inc

et décommentez la deuxième ligne

    include Make_msys2.inc

Si vous êtes sous environnement MacOS, commencez par installer homebrew si ce n'est déjà fait, puis installer g++ et openmpi :

    $ brew install gcc open-mpi

Éditer ensuite le fichier "Makefile" et commenter la première ligne :

    include Make.inc

et décommentez la troisième ligne

    include Make_osx.inc

NB : cela présuppose que vous ayez installé homebrew, puis g++ et opmenmpi au sein de homebrew.

Puis tapez

    make test

Si tout se passe bien, vous devriez avoir des sorties de divers programmes sur la console.

Si les messages vous semblent sortir *dans le désordre ou bien sont mélangés*, ne vous inquiétez pas,
**c'est un comportement tout à fait normal lorsqu'on lance des programmes en parallèle**. 

