# Ignoriere-Klammer-Fehler Preprozessor

Dieser Preprozessor macht, das dein Skript Klammer-Fehler ignoriert.
IN KEINEM FALL ändert dieser dein Skript oder korrigiert dein Skript auf magische Weise, es unterdrückt lediglich die Fehler im Log:

## Aufrufen

Du kannst den Ignoriere-Klammer-Fehler Preprozessor aufrufen in dem du in deinem Skript `#ignoreBracketErrors` einsetzt.
Dieser Preprozessoer is Datei-Spezifisch, daher beeinflusst er beim aufrufen in einer Datei nicht alle anderen Dateien (Zumindest nicht was den Prozessor belangt).

## Was macht er

Wenn der Preprozessoer in einer Datei aufgerufen wird, werden alle Klammer-Fehler, beim loggen der Fehler, unterdrückt.
Das verändert die betroffenen Zeilen in keinster Weise, der einzige Unterschied ist, das der Log, diese Zeilen nicht, angeben wird.