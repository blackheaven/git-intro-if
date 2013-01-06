!SLIDE subsection
# Navigation #

!SLIDE commandline
.notes Bouge HEAD et le working directory à REF
	$ git checkout REF
	$ git checkout master # Revient au point de départ

!SLIDE commandline
.notes remet le repository (HEAD + br/HEAD) et/ou l'index et/ou le working directory à REF
	$ git reset [MODE] [REF] [FICHIERS]

!SLIDE commandline
.notes Créé un commit avec les changement inverses de A (exclus) à B ou de HEAD à B
	$ git revert [A..]B

!SLIDE commandline
.notes affiche l'état courant des fichiers (ajouté, supprimé, modifié, non-tracé)
	$ git status

!SLIDE commandline
.notes affiche les logs, REFS peut être une expression
	$ git log [REFS]

!SLIDE commandline
.notes Afficher un commit
	$ git show [REF]

!SLIDE commandline
.notes Affiche les différences, REFS peut être une expression
	$ git diff [REFS] [FICHIERS]
