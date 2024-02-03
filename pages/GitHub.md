Alias:: [[Problemas con GitHub]]

- # Generar clave SSH
	- Hay varios métodos para crear claves pero para facilitarme la vida pongo el paso a paso
	- ssh-keygen -t ed25519 -C "litigiouniversal@gmail.com"
	- clip < "name".pub
	- eval $(ssh-agent -s)     /*Este método sólo sirve en linux*/
	- ssh-add "name"
	- ## Problemas
		- https://serverfault.com/questions/760027/ssh-why-isnt-it-trying-my-private-key
		- Me ocurrió lo mismo que a este tipo. Cuando probé el testeo que sugiere github me dió error y al intentar solucionar el error por medio del [instructivo](https://docs.github.com/en/authentication/troubleshooting-ssh/error-permission-denied-publickey) me fijé que no reconocía el nombre que yo le puse al archivo ssh, sólo reconoció el nombre por default de los distintos cifrados. Por lo que me da ha suponer que hay que ingresarlo de alguna manera a esa lista de ssh.
		-
-