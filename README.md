# Plantilla de desarrollo para GBA

Premisa: no quiero tener que instalar DevKitPro en local. Cualquiera con VSCode y Docker debería poder desarrollar, depurar y compilar la ROM, sin necesidad de instalar dependencias.

* `bin/dmake`: Hace el make mediante un contenedor Docker con la imagen devkitpro/devkitarm.
* `bin/ddebug`: Lanza el depurador también mediante dicho contenedor Docker.

He configurado las siguientes tasks de VSCode:

* `make debug`
* `make release`
* `make clean`

Si desarrollo abriendo el proyecto en el dev container, funciona el intellisense sin problema, y puedo navegar por el código de las librerías (libgba en este caso).

He intentado configurar el depurador, que se lanza pulsando F5. Sin embargo, aunque el depurador parece funcionar si lo arranco en local, al hacerlo desde VSCode obtengo este error:

```
Starting: "/Users/fede/projects/GBA/template/bin/ddebug" --interpreter=mi
the input device is not a TTY
"/Users/fede/projects/GBA/template/bin/ddebug" exited with code 1 (0x1).
```
