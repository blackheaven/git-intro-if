!SLIDE
.notes on va parler de dagues, oups pas ce genre

![Poignard](cut.gif)

!SLIDE
![Graphe](graph.jpg)

!SLIDE subsection
.notes Utilisé pour organiser les commits

# Directed acyclic graph #

Graphe orienté acyclique

!SLIDE
Fait partie du Back-end

!SLIDE
.notes rappel tout est SHA1

![SHA](chat.gif)

!SLIDE
# Chaque commit comprends
Un identifiant

!SLIDE
Un message associé

!SLIDE
Un auteur

!SLIDE
Un ensemble de références vers son tree lui même connaissant ses blobs

!SLIDE
Un ensemble de références vers ses ancêtres

!SLIDE
# Combien ?

!SLIDE
.notes 0 pour le premier commit

![Un commit](un.svg)

!SLIDE
.notes 1 pour les cas courrants

![Flux linéaire](file.svg)


!SLIDE
.notes n pour les merges, split = 2 commits avec un parent, merge = 1 commit avec un parent

![Branchement](branchement.svg)


!SLIDE
.notes acceder à un commit n'est rien de plus qu'un déplacement dans le graphe et faire un commit revient à modifier le graphe

Un commit = un noeud du graphe

!SLIDE
![Branchement](branchement.svg)

!SLIDE
.notes mais comment on y accède ?

![Perplexe](perplex.gif)


