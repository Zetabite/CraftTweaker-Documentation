# Das Wiki benutzen

Dieses Wiki ist dafür gemacht um einen Überblick zu schaffen, welche Möglichkeiten in CraftTweaker existieren und wofür sie benutzt werden können.

Es enthält zudem einige Beispiele für bestimmte Einträge um mehr Klarheit zu schaffen.

# Bedingungen
Bevor wir anfangen sind da ein paar Bedingungen die du dich gewöhnen solltest:

## ZenGetter
Ein ZenGetter ist eine Möglichkeit um Informationen von bestimmten Objekten zu erhalten. Zum Beispiel hat [IItemStack](/Vanilla/Items/IItemStack/) einen ZenGetter der "displayName" genannt wird.

Wir benutzen die ZenGetter wie folgt:
```
//object.zenGetter;
<minecraft:iron_ingot>.displayName;
```

Ein ZenGetter wird immer irgendwas zurückgeben, in diesem Fall einen String(Zeichenabfolge), der den Namen des Items repräsentiert ("Eisen Barren").

## ZenSetter
Ein ZenSetter funktioniert ähnlich wie ein ZenGetter, der einzige Unterschied besteht darin, das ein ZenSetter etwas einsetzt, ein ZenGetter etwas zurückgibt.

Lass uns bei dem [IItemStack](/Vanilla/Items/IItemStack/) bleiben, denn es existiert auch ein ZenSetter mit dem Namen "displayName". Wir wissen von dem Eintrag, das es sich hierbei um einen String handelt.  

Wir benutzen den ZenSetter etwa so:
```
//object.zenSetter = newValue;
<minecraft:iron_ingot>.displayName = "Unscheinbarer Barren";
```

Ein ZenSetter wird nie etwas zurückgben, da ist nur zum einsetzen, aber nicht fürs zurückgeben, gemacht ist.

## Festlegende Operatoren
Wenn ein Item sowohl einen ZenGetter als auch einen ZenSetter mit dem selben Namen (z.B. [IItemStack's](/Vanilla/Items/IItemStack/) "displayName") hat, kannst du einen der Festlegenden Operatoren nutzen, die nicht `=` sind:

Abhänging von der Art, kannst du folgende benutzen: `&=`, `|=`, `+=`, `-=`, `*=`, `/=`, `%=`, `~=`.

Lass und mal schauen, was sie tun:

```
//Da wir einen ZenGetter und einen ZenSetter mit dem selben Namen vorliegen haben, tun der Erste und der Zweite das gleiche:
//object.zenSetter += wert;
//object.zenSetter = object.zenGetter + wert;

//Beispiel 1:
<minecraft:iron_ingot>.displayName += " des Untergangs";

//Beispiel 2:
<minecraft:iron_ingot>.displayName = <minecraft:iron_ingot>.displayName + " des Untergangs";
```
In beiden Beispielen wird am Ende der Eisen Barren jeweils "Eisen Barren des Untergangs" heißen.
