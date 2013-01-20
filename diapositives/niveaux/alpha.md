!SLIDE subsection
.notes Concept le plus dur à retenir

# Niveaux #

!SLIDE
.notes Rappel : git est un simple gestionnaire de cache

![Niveaux](niveaux.svg)

!SLIDE commandline
.notes Ajoute main.c à l'index

	$ git add main.c

!SLIDE commandline
.notes Crée un commit à partir de l'index ; Crée un commit à partir de la copie de travail

	$ git commit
	$ git commit -a

!SLIDE commandline
.notes Ajoute main.c à l'index

	$ git add main.c

!SLIDE commandline
.notes Différence par rapport au dépôt (dernier commit)

	$ git diff main.c

!SLIDE commandline
.notes Différence par rapport à l'index (commit courant)

	$ git diff --cached main.c

!SLIDE commandline
.notes Affiche l'état des fichiers / wat ?! / le premier est l'index, l'autre la copie de travail

	$ git add main.c
	$ vi main.c
	$ git status
	# On branch master
	# Changes to be committed:
	#   (use "git reset HEAD <file>..." to unstage)
	#
	#	modified:   main.c
	#
	# Changes not staged for commit:
	#   (use "git add <file>..." to update what will be committed)
	#   (use "git checkout -- <file>..." to discard changes in working directory)
	#
	#	modified:   main.c
	#

!SLIDE
# Stash

!SLIDE bullets
  * Espace temporaire
  * Extrait les modifications de la copie de travail
  * Peu utilisé en faveur des branches
