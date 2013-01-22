!SLIDE subsection
# Références et reflog #
!SLIDE

un commit ne connait que ses parents, on peut donc en perdre

!SLIDE
.notes NON !

# Reflog

!SLIDE
.notes Le reflog contient toutes les actions effectuées localement durant des mois

	$ git reflog
	5a94ead HEAD@{0}: commit: msg
	faa47ea HEAD@{1}: commit: msg
	f776321 HEAD@{2}: commit: msg
	d10408b HEAD@{3}: commit: msg
	c3464d6 HEAD@{4}: commit: msg
	174c0b1 HEAD@{5}: commit: msg

!SLIDE commandline
.notes Permet de voir le commit en question

	$ git show HEAD@{4}

!SLIDE
.notes Impossible de perdre quoi que ce soit et de devoir refaire un clone, fini les detached HEAD

![La classe](chat_.gif)

!SLIDE

## Les remotes

!SLIDE commandline
.notes .git indique un dépôt partagé

	$ git remote # Liste
	$ git remote add foo https://github.com/bar/baz.git # Ajoute
	$ git remote rm foo # Supprime

!SLIDE commandline
.notes push toutes les branches ; master sur origin/b1 ; idem pour fetch

	$ git push origin --all
	$ git push origin master:origin/b1
	# Ou
	$ vi .git/config
	[remote "origin"]
	    push = refs/heads/master:refs/heads/origin/b1
	
	$ git push origin master

