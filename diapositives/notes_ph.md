Conférence git
==============

20
--
Noyau Linux hébergé sur Bitkeeper. Mais contrat non renouvelé pour certains dév.
=> Décision de Linus Torvald d'héberger le noyau sur son propre gestionnaire de
versions. git était né (2005).

21
--
* Plumbing (commandes de backend) fait par L. Torvald (en gal plus utilisées,
mais encore disponibles)
* Porcelain (commandes de frontend) fait par la communauté des dev git (en gal
utilisées à la place du backend)

26
--
git => gestionnaire de contenu.

27
--
1036 lignes de C => mettre et enlever du contenu dans des fichiers et c'est tout.

40
--
Utilisé pour organiser les commits.

65
--
Branches de git différentes de celles de Mercurial.

75
--
Création d'une branche ou d'un tag ne prend que 40 octets.

79
--
Transition vers remote.

81 et suivantes
---------------
Insister sur les notions de remote et de namespaces.

88
--
Alias permet de raccourcir les noms. Différence avec un tag: un alias est attaché à une
branche donnée.

Remote = Namespace avec des branches.
Les branches du remote n'ont aucun rapport pré-défini avec les branches localeS.
Par exemple: pour un dépôt git ayant des branches master et b1, et un dépôt local avec
master, b1 et b2, l'utilisateur peut décider de merger la branche remote de github b1
sur la branche locale b2 avec la commande `git pull b2:github/b1'.

90
--
Poser la question : "Que fait cette commande ?"

93
--
Fonction de add dépend du contexte (index ou trace).

96
--
diff par wd / repository

97
--
diff catch wd / index

98
--
Question: Pourquoi ça fait ça ?
