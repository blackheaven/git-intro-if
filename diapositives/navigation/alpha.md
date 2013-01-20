!SLIDE subsection
# Navigation #

!SLIDE commandline
.notes Bouge HEAD et le working directory à REF

	$ git checkout REF
	$ git checkout master # Revient au point de départ

!SLIDE commandline
.notes Remet le dépôt (HEAD + br/HEAD) et/ou l'index et/ou la copie de travail à REF

	$ git reset [MODE] [REF] [FICHIERS]

!SLIDE commandline
.notes Crée un commit avec les changements inverses de A (exclus) à B ou de HEAD à B

	$ git revert [A..]B

!SLIDE commandline
.notes Affiche l'état courant des fichiers (ajouté, supprimé, modifié, non-tracé)

	$ git status

!SLIDE commandline
.notes Affiche les logs, REFS peut être une expression

	$ git log [REFS]

!SLIDE commandline
.notes Afficher un commit

	$ git show [REF]

!SLIDE commandline
.notes Affiche les différences, REFS peut être une expression

	$ git diff [REFS] [FICHIERS]
