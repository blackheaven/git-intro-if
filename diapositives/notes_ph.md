Conf�rence git
==============

20
--
Noyau Linux h�berg� sur Bitkeeper. Mais contrat non renouvel� pour certains d�v.
=> D�cision de Linus Torvald d'h�berger le noyau sur son propre gestionnaire de
versions. git �tait n� (2005).

21
--
* Plumbing (commandes de backend) fait par L. Torvald (en gal plus utilis�es,
mais encore disponibles)
* Porcelain (commandes de frontend) fait par la communaut� des dev git (en gal
utilis�es � la place du backend)

26
--
git => gestionnaire de contenu.

27
--
1036 lignes de C => mettre et enlever du contenu dans des fichiers et c'est tout.

40
--
Utilis� pour organiser les commits.

65
--
Branches de git diff�rentes de celles de Mercurial.

75
--
Cr�ation d'une branche ou d'un tag ne prend que 40 octets.

79
--
Transition vers remote.

81 et suivantes
---------------
Insister sur les notions de remote et de namespaces.

88
--
Alias permet de raccourcir les noms. Diff�rence avec un tag: un alias est attach� � une
branche donn�e.

Remote = Namespace avec des branches.
Les branches du remote n'ont aucun rapport pr�-d�fini avec les branches localeS.
Par exemple: pour un d�p�t git ayant des branches master et b1, et un d�p�t local avec
master, b1 et b2, l'utilisateur peut d�cider de merger la branche remote de github b1
sur la branche locale b2 avec la commande `git pull b2:github/b1'.

90
--
Poser la question : "Que fait cette commande ?"

93
--
Fonction de add d�pend du contexte (index ou trace).

96
--
diff par wd / repository

97
--
diff catch wd / index

98
--
Question: Pourquoi �a fait �a ?
