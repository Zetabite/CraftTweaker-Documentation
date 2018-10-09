# Loader Preprozessor

Der Loader Preprozessor wird den Skript Loader setzen.

## Aufrufen

Du rufst den Loader Preprozessor auf, in dem du `#loader loaderName` in dem Skript einfügst, mit `loaderName` als Namen des Loaders denn du dem Skript zuweisen möchtest.
Beispiel: `#loader ContentTweaker`

## Was macht er

Skripte mit Loader Preprozessoer werden nur geladen wenn sie vom Loader spezifiziert werden.
In dem oberen Beispiel würde CraftTweakers Loader die Datei nicht ausführen, stattdessen wird der Loader "ContentTweaker" dieses Skript ausführen.
Wenn du den Preprozessor nicht spezifizierst, wird standardmäßig "crafttweaker" verwendet.