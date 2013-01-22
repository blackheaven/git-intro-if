!SLIDE
.notes On va parler de dagues, oups pas ce genre

![Poignard](cut_.gif)

!SLIDE
![Graphe](graph.jpg)

!SLIDE subsection
.notes Utilisé pour organiser les commits

# Directed acyclic graph #

Graphe orienté acyclique

!SLIDE
Fait partie du backend

!SLIDE
.notes Rappel : tout est SHA-1

![SHA](chat_.gif)

!SLIDE
# Chaque commit comprend
Un identifiant

!SLIDE
Un message associé

!SLIDE
Un auteur

!SLIDE
Un ensemble de références vers son tree, lui-même connaissant ses blobs

!SLIDE
Un ensemble de références vers ses ancêtres

!SLIDE
# Combien ?

!SLIDE
.notes 0 pour le premier commit

![Un commit](un.svg)

!SLIDE
.notes 1 pour les cas courants

![Flux linéaire](file.svg)

!SLIDE
.notes N pour les merges, split = 2 commits avec un parent, merge = 1 commit avec un parent

![Branchement](branchement.svg)

!SLIDE
.notes Accéder à un commit n'est rien de plus qu'un déplacement dans le graphe et faire un commit revient à modifier le graphe

Un commit = un nœud du graphe

!SLIDE
![Branchement](branchement.svg)

!SLIDE
.notes Mais comment on y accède ?

![Perplexe](perplex_.gif)
