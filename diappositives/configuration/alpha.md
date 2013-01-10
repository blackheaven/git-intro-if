!SLIDE subsection
# Configuration #

!SLIDE commandline
.notes Git ne possède pas de moyen d'authentification de base

	$ git config --global user.name "John Doe"
	$ git config --global user.email johndoe@example.com

!SLIDE commandline
.notes permet de mettre des messages de commit et de faire les fusions

	$ git config --global core.editor vim
	$ git config --global merge.tool vimdiff
	$ git config --global color.ui true

