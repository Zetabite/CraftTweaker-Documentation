# Alles über Preprozessor

## Was sind Preprozessor

Wie der Name vermuten lässt, werden Preprozessoren ausgeführt, bevor das Skript ausgeführt wird.
Sie können verschiedene Aktionen ausführen, zum Beispiel den Debug Modus aktiviern, oder Klammer-Fehler unterdrücken.

## Einen Preprozessor aufrufen

Ein Preprozessor kann mit der #Kommentar Funktion, aufgerufen werden.
Sei also vorsichtig mit #Kommentaren, es könnte sein das du einen Preprozessor mit einem Schlüsselwort aufrufst! 

Beispiel:
```JAVA
#debug ist mein Lieblings Anglezismus, am liebsten würde ich ihn überall als Kommentar einfügen
```

↑ Das würde den Debug Modus aktivieren da `#debug` gefunden wurde. Wenn du wirklich sichergehen möchtest, das ein solch seltener Fall passiert, benutze am besten `//` für Kommentare