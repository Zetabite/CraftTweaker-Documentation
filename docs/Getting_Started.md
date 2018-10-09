# Erste Schritte mit den Skripte

Crafttweaker benutzt eine eigene Programmiersprache, sie nennt sich `ZenScript / ZenSkript`, ZenScript liest `.zs` Dateien, die in dem Ordner `<minecraftdir>/scripts>` gespeichert sind.

ZenScript ist eine "top down" Programmiersprache, das heißt, `Imports` müssen ganz oben in der Datei sein, `Variablen Deklarationen` sollten weiter oben eingeführt werden.
Eigentlich ist es egal wo du die `Variable` definierst, nur ist sie in den Zeilen über ihrer `Variablen Deklaration` nicht zugänglich bzw. nicht benutzbar.

## Einführung

Hast du schon mal ein Modpack zusammen gestellt und gemerkt das das einfache zusammen werfen von Mods dir das Gefühl gegeben hat, das sie nicht ganz miteinander interagieren?
Da Mods von eindander unabhängig programmiert werden, kann sich eine Mod im Verhältnis zu einer anderen sehr oder zu stark an fühlen, "Overpowered".
Oder du meinst manche Items(Gegenstände) ein besseres Rezept haben könnten?
Vielleicht willst du ja sogar ein Item aus dem Spiel entfernen, ohne die ganze Mod zu entfernen.
Manchmal findest du Einträge im `Ore Dictionary`(Lexion für Minecraft um Items in Kategorien ein zu ordnen, um zum Beispiel Rezept Bestandteile mit einem Item der selben Kategorie zu verwenden zu können), die zu viele oder zu wenige Items haben.
Nun kannst du all das bearbeiten - mit nur einer Anweisung in CraftTweaker.

Zusätzlich zu den den Kern Funktionen, die Vanilla Minecraft unterstützen, werden auch Mod Einbindungs Bibliotheken geboten, die, wenn die Mod aktiviert ist, nicht nur Vanilla Rezepte verändern, sondern auch Mod Maschinen-Rezepte und Mod-Verhalten.

## Skripte

Skripte sind in `<minecraftdir>/scripts` aufbewahrt und werden in der `PreInitialization` Phase von Minecraft geladen, im Gegensatz zu vorigen Versionen von CraftTweaker, können Skripte nicht mehr im Spiel neu geladen werden, durch Änderungen die Mojang in der Version 1.12 vorgenommen hat und es keinen anderen Weg gibt es wieder zu implementieren.
Zudem müssen Skripte **sowohl, auf dem Server ALS AUCH auf der Client-Instanz** vorhanden sein, um zu funktionieren.

Skripte haben den die Dateiendung `.zs` und können auch als komprimierte `.zip` gelesen werden.

### Schreibe dein erstes Skript

Um mit dem Programmieren anzufangen, kannst du ein einfach Datei erstellen, mit dem Namen `hallo.zs`, in dem Ordner `<minecraftdir>/scripts>`.

Schreib in `hallo.zs` in die folgenden Zeilen:
```
print("Hallo Welt!");
```

Starte jetzt Minecraft und schau dir die Datei `crafttweaker.log` in deinem `<minecraftdir>` an. Diese kann in jedem Programm eingesehen werden, die Klartext Dateien lesen kann.

Wir empfehlen das du die Skripte mit Visual Studio Code, Notepad++ oder Sublime Text bearbeitest, aber eigentlich kannst du dies mit jedem Textbearbeitungs Programm.

### Die Datei crafttweaker.log

Die Datei `crafttweaker.log` benutzt eine besondere Syntax(Bauform/Satzbau) in ihrer Ausgabe, diese Syntax ist wie folgt:
```
[LOADERSTAGE][SIDE][TYPE] <nachricht>
```

Wenn du das Beispiel von oben benutzt, würde die Ausgabe so aussehen:
```
[PREINITIALIZATION][CLIENT][INFO] Hallo Welt!
```

Die Syntax wird vor allem zum Zweck des Debuggen(Fehler beheben) benutzt und wird nur allein für die Ausgabe von Kommandos, in diesem Fall würde es nur die Nachricht schreiben, das ist so, um das Kopieren und Einfügen einfacher zu gestalten.

### Kommentare

Kommentare können und sollten benutz werden um Skripte lesbar und einfacher verständlich zu machen!

ZenScript unterstüzt 3 Arten von Kommentaren:

Einzeiler: `// Ich bin ein Einzeiler Kommentar`

Alternativer Einzeiler: `# Ich bin auch ein Einzeiler Kommentar!`

Mehrzeiler Kommentar: 
```
/* Ich
bin
ein
Mehrzeiler Kommentar! */
```