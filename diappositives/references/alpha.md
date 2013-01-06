!SLIDE subsection
.notes concept le plus dur à apréhender
# Références #

!SLIDE
Fait partie du front-end

!SLIDE
# SHA1

!SLIDE
.notes Peut être abrégé
8f48c3097fb9f09a8eefbb4ad2023638981e704c
8f48c

!SLIDE
Tout a une référence (fichier, commit, objets)

!SLIDE
Toute référence est unique

!SLIDE
.notes en partant de ce constat comment sait où on est dans le graphe ? indice : un commit ne connait sa branche
TODO : IMG perdu (plan énorme avec vous ête ici)

!SLIDE
.notes Le HEAD : dernier commit d'une branche
TODO : IMG mais où ais-je la tête

!SLIDE commandline
.notes HEAD : référence courante
	$ cat .git/HEAD
	ref: refs/heads/master

!SLIDE commandline
.notes chaque branche à son HEAD
	$ cat .git/refs/heads/master
	35ee8ce6b66480fc67eea935431fad16a9ee44c0

!SLIDE
TODO : IMG deux branches sans merge avec chacunes un branche/HEAD + une des deux avec HEAD

!SLIDE
mini langage de manipulation

!SLIDE commandline
.notes Commit n - 1 ; git show : voir un commit ; HEAD peut être n'importe quel référence (Tag, SHA1, etc.)
	$ git show HEAD~1

TODO : IMG 1 branche avec n commit, HEAD + HEAD - 1

!SLIDE commandline
.notes 2ème parent
	$ git show HEAD^2

TODO : IMG 2 branches avec n commit, HEAD + 2ème parent

!SLIDE commandline
.notes équivalents
	$ git show HEAD^1
	$ git show HEAD^
	$ git show HEAD

!SLIDE commandline
.notes équivalents
	$ git show HEAD^2
	$ git show HEAD^^

!SLIDE commandline
.notes Interval ; log = liste des commits
	$ git log 2a32..8f48

TODO : IMG 1 branche avec n commit, HEAD + 2a exclus 8f inclus

!SLIDE commandline
.notes peut devenir complexe
	$ git log HEAD~8^3..HEAD~2^2

!SLIDE commandline
.notes Plusieurs types de références
	$ ls .git/refs
	heads
	remotes
	tags

!SLIDE
# Tags

!SLIDE
.notes moyen d'accès rapide à un commit
TODO : IMG n commits, une branche, un br/HEAD + TAG V1.0

!SLIDE
Différence entre un HEAD et un Tag ?

!SLIDE
.notes HEAD est déplace automatiquement, Tag manuellement
L'utilisateur !

!SLIDE
.notes rappel : un commit ne connais que son/ses ancêtre(s)
Mais le Dag ?

!SLIDE
.notes une référence est perdu à jamais, il y a un ramasse miette qui supprime toutes les références inacessibles au bout d'un certain temps
TODO : IMG (le noooooon de luke)

!SLIDE
.notes Outil le plus puissant de Git disponible uniquement sur Git et Darc
# Remotes

!SLIDE
.notes s'ajoute au Dag
1 seul Dag

TODO : IMG 2 branches master et remote/master

!SLIDE
.note notions importante
# Namespaces

!SLIDE
.notes on ajoute un remote puis on fetch (reception) ou push (envoi)
  * fetch
  * push

!SLIDE
  * pull = fetch + merge
  * pul=sh

!SLIDE
une branche à la fois

!SLIDE commandline
.notes rappel
	$ cat .git/HEAD
	ref: refs/heads/master

!SLIDE
# Alias

!SLIDE commandline
.notes master devient origin/b2
	$ git pull origin master:origin/b2
	$ git push origin master:origin/b2

!SLIDE
.notes de manière générale
<source>:<destination>

!SLIDE commandline
.notes attention : supprime la branche
	$ git push origin :origin/b2

