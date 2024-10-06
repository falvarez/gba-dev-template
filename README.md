# Plantilla de desarrollo para GBA

Premisa: no quiero tener que instalar DevKitPro en local. Cualquiera con VSCode y Docker debería poder desarrollar, depurar y compilar la ROM, sin necesidad de instalar dependencias.

* `bin/dmake`: Hace el make mediante un contenedor Docker con la imagen devkitpro/devkitarm.
* `bin/ddebug`: Lanza el depurador también mediante dicho contenedor Docker.

He configurado las siguientes tasks de VSCode:

* `make debug`
* `make release`
* `make clean`

He intentado configurar el depurador 

* Intellisense sólo va a funcionar dentro del contenedor docker
* Puedo hacer make dentro y fuera, si configuro ambos
* No consigo lanzar el depurador: me dice que el proceso no es un tty. ¿Tiene solución esto?