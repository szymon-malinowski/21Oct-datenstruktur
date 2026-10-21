# 21Oct-datenstruktur: Wichtige Punkte

## Ziele dieser Lektion

Nach dieser Lektion kannst du:

1. Arrays, `Map`/Objekte, `Set`, Stacks, Queues und verkettete Listen anhand ihrer Grundidee und typischen Einsatzzwecke unterscheiden.
2. das LIFO-Prinzip eines Stacks erklären und beschreiben, warum ein Stack mit einem Array umgesetzt werden kann.
3. einen einfachen Stack mit `push()`, `pop()`, `peek()`, `isEmpty()` und `size()` in JavaScript implementieren und verwenden.
4. die Schritte einer linearen Suche erklären und in einem Array einen Wert oder Datensatz finden.
5. beschreiben, wie Bubble Sort benachbarte Werte vergleicht und vertauscht, und den Algorithmus in JavaScript umsetzen.
6. den ungefähren Laufzeit- und Speicherbedarf einfacher Operationen mit `O(1)`, `O(n)` und `O(n²)` einordnen.

## Verständnisfragen

1. Worin unterscheiden sich Array, `Map`/Objekt und `Set` hinsichtlich der Art, wie Daten organisiert oder gefunden werden?
2. Was bedeutet LIFO, und welche Werte liefert ein Stack nach `push("A")`, `push("B")`, `push("C")` und anschließendem zweimaligem `pop()`?
3. Warum greift `peek()` auf `this.items[this.items.length - 1]` zu, und wie reagiert die Beispielklasse auf einen leeren Stack?
4. Wie unterscheidet sich die Rückgabe von `linearSearch()` von der Rückgabe von `findUserById()`, wenn kein Treffer gefunden wird?
5. Warum ist Bubble Sort für große Listen ineffizient, und wie wirkt sich `[...array]` auf den zusätzlichen Speicherbedarf und das Original-Array aus?
