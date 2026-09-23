Mods VIKINGOSFURIOSOS - Instalación en Linux (Steam)
======================================================

1) COPIAR ARCHIVOS
   Copiá "BepInEx", "winhttp.dll" y "doorstop_config.ini" directamente
   dentro de la carpeta de instalación de Valheim (la misma carpeta
   donde está el .exe o el ejecutable del juego), pisando lo que haya.

   Se puede encontrar la carpeta desde Steam: click derecho en Valheim
   -> Administrar -> Explorar archivos locales.

2) FORZAR PROTON
   En Steam: click derecho en Valheim -> Propiedades -> pestaña
   Compatibilidad -> tildar "Forzar el uso de una herramienta de
   compatibilidad de Steam Play específica" -> elegir cualquier
   Proton reciente (Proton Hotfix, Proton Experimental o el último
   Proton numerado).

   IMPORTANTE: tiene que ser Proton, no el binario nativo de Linux
   del juego. El mod de voz (Proximity Voice Chat) necesita una API
   de audio de Windows que solo existe corriendo bajo Proton/Wine.

3) OPCIONES DE LANZAMIENTO (el paso que más rompe si se salta)
   En la misma pantalla de Propiedades, pestaña General, en
   "Opciones de lanzamiento" pegar EXACTAMENTE esto:

       WINEDLLOVERRIDES="winhttp=n,b" %command%

   Sin esto, Wine usa su propio winhttp.dll en vez del de BepInEx
   y ningún mod carga (el juego abre pero "no toma los mods").

4) JUGAR
   Dale a Jugar normal desde Steam. El primer arranque bajo Proton
   puede tardar más de lo normal (arma el prefix la primera vez).

Para chequear que los mods cargaron bien: abrí
BepInEx/LogOutput.log después de una partida y confirmá que dice
"Loading [Jotunn ...]", "Loading [Valheim Plus ...]", etc. sin
errores de DllNotFoundException.
