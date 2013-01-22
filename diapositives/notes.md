Conférence git
==============

1
--
Gautier et Pierre-Henri, membre de l'équipe technique de l'AEDI.

On fait cette conférence suite au constat que le temps nous manque pour comprendre Git.

10
--
Le but est de mieux utiliser git, pas de l'utiliser tout le temps.

Une solution résout un problème.

18
--
La première chose à laquelle on pense lorsque l'on pense à git, c'est : "compliqué"

20
--
Noyau Linux hébergé sur Bitkeeper. Mais contrat non renouvelé pour certains dev.

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
==> PH

git => gestionnaire de contenu.

27
--
1 036 lignes de C : seulement un système d'interrogation et de manipulation de cache

34
--
Vous vous dites : ça prends trop de place !

37
--
Je vous ai menti, compression à la MPEG : 1 snapshot, N diffs, 1 snapshot

Du coups ça prends peu de place

====> parlons de dag

40
--
Utilisé pour organiser les commits.

42
--
Rappel tout est sha1

51
--
N pour les merges, split = 2 commits avec un parent, merge = 1 commit avec un parent

54
--
Mais comment on y accède ?

55
--
==> G

Concept le plus dur à appréhender

61
--
En partant de ce constat, comment sait-on où on est dans le graphe ? Indice : un commit ne pas connait sa branche

Branches de git différentes de celles de Mercurial.

75
--
Création d'une branche ou d'un tag ne prend que 40 octets.

77
--
HEAD est déplacé automatiquement, Tag manuellement

79
--
Quand une référence est perdue à jamais, elle est supprimée.

Il y a un ramasse-miettes qui supprime toutes les références inaccessibles au bout d'un certain temps.

====> Ce problème est bien épineux, faisons une pause sur le dag avant de résoudre ce soucis.

80
--
Outil le plus puissant de git disponible uniquement sur git et Darc

81 et suivantes
---------------
Insister sur les notions de remote et de namespaces.
Les remotes posent un soucis : le remote peut avoir les mêmes nom des branches, donc il faut créé une notion de namespace comment en C++.

86
--
Rappel : on manipule des refs, maiis ça peut être long avec les NS

88
--
Alias permet de raccourcir les noms. Différence avec un tag: un alias est attaché à une
branche donnée.

Remote = Namespace avec des branches.

Les branches du remote n'ont aucun rapport pré-défini avec les branches locales.

Par exemple: pour un dépôt git ayant des branches master et b1, et un dépôt local avec

master, b1 et b2, l'utilisateur peut décider de merger la branche remote de github b1

sur la branche locale b2 avec la commande 'git pull b2:github/b1'.

90
--
Poser la question : "Que fait cette commande ?"

91
--
==> PH

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

104
--
git ne possède pas de moyen d'authentification de base

105
--
Permet de mettre des messages de commit et de faire les fusions

107
--
Bouge HEAD et le working directory à REF

108
--
Remet le dépôt (HEAD + br/HEAD) et/ou l'index et/ou la copie de travail à REF

109
--
Crée un commit avec les changements inverses de A (exclus) à B ou de HEAD à B

110
--
Affiche l'état courant des fichiers (ajouté, supprimé, modifié, non-tracé)

111
--
Affiche les logs, REFS peut être une expression

112
--
Afficher un commit

113
--
Affiche les différences, REFS peut être une expression

115
--
liste les branches

118
--
renomme la branche

122
--
pourquoi ? on a fait un commit sur aucune branche, donc il est inaccessible sans sa référence

123
--
as-t-on une alternative au grand saut ?

124
--
==> G

131
--
.git indique un dépôt partagé, fait par init --bare

on peut push sur un dépôt partagé, mais on ne peut que pull sur un dépôt normal

un dépôt partagé n'a pas de working directory

132
--
push toutes les branches

master sur origin/b1

idem pour fetch

136
--
Fast forward par défaut sur merge

commit sur pull

les plus utilisés en haut

139
--
réécrit les commits

En cas de conflit, on le résout commit par commit

utilisez le

140
--
Sinon ça rajoute des commits inutiles au Dag en ajoutant de simple merge sans résollution de conflits
