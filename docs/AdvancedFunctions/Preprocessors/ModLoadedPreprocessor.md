# Mod-Loader Preprozessor

Der Mod-Loader Preprozessoer führt nur ein Skript aus, wenn eine bestimmte Mod vorhanden ist.

## Aufrufen

Der Mod-Loader Preprozessoer kann hinzufügefügt werden, in dem du `#modloaded modID` in dein Skript schreibst, mit `modID` als die die ModID, die du überprüfen möchtest:
Beispiel: `#modloaded minecraft`

Du kannst sogar mehrere ModIDs überprüfen lassen:
`#modloaded minecraft tconstruct` wird nur ausgeführt wenn Minecraft UND Tinker's Construct geladen sind.

Du kannst aber auch eine Mod Kondition invertieren, sodass das Skript nur geladen wird, wenn die Mod NICHT geladen wurde:
`#modloaded !tconstruct minecraft` wird nur ausgeführt wenn Minecraft geladen und Tinker's Construct nicht geladen ist.

## Was macht er

Dieser Preprozessor führt das Skript nur aus, wenn die gegebenen ModIDs geladen, oder nicht geladen sind, mit anderen Worten die Mods geladen oder nicht geladen sind.