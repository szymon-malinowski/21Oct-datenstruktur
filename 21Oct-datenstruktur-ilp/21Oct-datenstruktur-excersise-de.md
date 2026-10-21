# Individuelle Learning Phase: Datenstrukturen und Grundalgorithmen in Node.js

## Dein Ziel

Du entwickelst ein kleines Node.js-Skript zur Analyse von API-Requests. Dabei arbeitest du mit Arrays, vergleichst einfache Datenstrukturen, implementierst eine lineare Suche, sortierst Daten mit Bubble Sort und baust einen eigenen Stack nach dem LIFO-Prinzip.

## Das brauchst du

- Node.js
- einen Code-Editor
- ein Terminal
- einen Projektordner, z. B. `request-analyzer`
- Grundkenntnisse in JavaScript und dem Starten von Node.js-Dateien mit `node datei.js`

## Zeitplanung

- **10 Minuten:** Projekt anlegen und Datenbasis vorbereiten
- **20 Minuten:** Arrays untersuchen und einfache Strukturvergleiche festhalten
- **20 Minuten:** Lineare Suche implementieren und testen
- **25 Minuten:** Bubble Sort für Request-Dauern umsetzen
- **25 Minuten:** Stack in JavaScript implementieren
- **20 Minuten:** Alles in einem kleinen Analyse-Skript zusammenführen

## Basis-Aufgaben

### Aufgabe 1:

Datenbasis vorbereiten  
**Ziel:** Du erstellst eine realistische Grundlage für alle weiteren Aufgaben.  
**Arbeitsauftrag:** Lege eine Datei `requests.js` oder `app.js` an und erstelle ein Array mit mindestens 10 Request-Objekten. Jedes Objekt soll z. B. diese Felder enthalten: `id`, `route`, `method`, `status`, `durationMs`. Nutze realistische Werte wie `/users`, `/login`, `/orders`, `GET`, `POST`, Statuscodes und unterschiedliche Laufzeiten. Gib das komplette Array in der Konsole aus.  
**Erwartetes Ergebnis / Soll-Zustand:** Du hast ein lauffähiges Node.js-Skript mit einem Array aus mindestens 10 Request-Objekten, das fehlerfrei ausgegeben wird.

### Aufgabe 2:

Arrays und grundlegende Strukturvergleiche  
**Ziel:** Du erkennst, wie Arrays arbeiten und wofür ein Stack im Vergleich sinnvoll ist.  
**Arbeitsauftrag:** Erweitere dein Skript um kurze Codebeispiele mit deinem Request-Array:
- füge einen neuen Request hinzu
- entferne den letzten Request
- greife auf den ersten und letzten Eintrag zu
- gib die Anzahl der Requests aus

Erstelle zusätzlich in einer Datei `notizen.md` oder als Kommentarblock im Code einen kurzen Vergleich:
- Wofür ist ein Array praktisch?
- Wofür wäre ein Stack in einem Backend-Szenario praktischer?
- Nenne mindestens ein Beispiel aus dem Backend, z. B. Verlauf letzter Aktionen, Undo-Schritte, Rücksprunglogik oder zuletzt verarbeitete Jobs.  
**Erwartetes Ergebnis / Soll-Zustand:** Du hast funktionierenden Code für typische Array-Operationen und einen kurzen, verständlichen Vergleich zwischen Array-Nutzung und Stack-Nutzung.

### Aufgabe 3:

Lineare Suche für Request-IDs  
**Ziel:** Du implementierst eine einfache Suchfunktion für unsortierte Daten.  
**Arbeitsauftrag:** Schreibe eine Funktion `findRequestById(requests, id)`, die das Array linear durchsucht und den passenden Request zurückgibt. Falls nichts gefunden wird, soll ein sinnvoller Rückgabewert oder eine passende Meldung ausgegeben werden. Teste die Funktion mit:
- einer vorhandenen ID
- einer nicht vorhandenen ID

Erweitere die Funktion optional so, dass du zusätzlich nach einer Route suchen kannst, z. B. `/users`.  
**Erwartetes Ergebnis / Soll-Zustand:** Du kannst unsortierte Request-Daten per linearer Suche durchsuchen und bekommst nachvollziehbare Ergebnisse in der Konsole.

### Aufgabe 4:

Bubble Sort für Request-Dauern  
**Ziel:** Du sortierst Daten schrittweise mit einem einfachen Sortieralgorithmus.  
**Arbeitsauftrag:** Erstelle eine Funktion, die deine Requests nach `durationMs` mit Bubble Sort aufsteigend sortiert. Arbeite zunächst direkt mit einem Array von Zahlen oder sortiere die Request-Objekte anhand ihres `durationMs`-Werts. Gib vor und nach dem Sortieren die Reihenfolge aus.

Ergänze danach eine kurze Einschätzung in `notizen.md` oder im Kommentar:
- Wie viele Vergleiche fallen bei wenigen Daten ungefähr an?
- Warum ist Bubble Sort für große Datenmengen eher unpraktisch?
- Braucht deine Lösung zusätzlichen Speicher oder sortierst du direkt im vorhandenen Array?  
**Erwartetes Ergebnis / Soll-Zustand:** Du hast eine funktionierende Bubble-Sort-Implementierung und kannst die sortierten Laufzeiten bzw. Requests in aufsteigender Reihenfolge ausgeben.

### Aufgabe 5:

Eigenen Stack in JavaScript umsetzen  
**Ziel:** Du setzt das LIFO-Prinzip praktisch um.  
**Arbeitsauftrag:** Implementiere eine eigene Stack-Struktur als Klasse oder Factory-Funktion, z. B. `Stack`. Baue mindestens diese Methoden ein:
- `push(element)`
- `pop()`
- `peek()`
- `isEmpty()`
- `size()`

Nutze den Stack anschließend für ein kleines Backend-nahes Beispiel: Speichere die zuletzt verarbeiteten Requests auf dem Stack. Lege mindestens 5 Requests nacheinander ab, gib den obersten Eintrag mit `peek()` aus und entferne danach zwei Einträge mit `pop()`.  
**Erwartetes Ergebnis / Soll-Zustand:** Du hast eine eigene Stack-Implementierung, die korrekt nach dem LIFO-Prinzip arbeitet und mit deinen Request-Daten getestet ist.

### Aufgabe 6:

Mini-Analyse-Skript zusammenführen  
**Ziel:** Du verbindest Datenstruktur und Algorithmen in einem kleinen Node.js-Werkzeug.  
**Arbeitsauftrag:** Erstelle eine Datei `analyzeRequests.js`, in der du die bisherigen Bausteine zusammenbringst. Das Skript soll beim Start mindestens Folgendes tun:
- alle Requests laden
- einen Request per linearer Suche finden
- alle Requests nach `durationMs` sortieren
- die 3 langsamsten Requests ausgeben
- einen Stack mit den zuletzt verarbeiteten Requests demonstrieren

Strukturiere den Code übersichtlich mit Funktionen und aussagekräftigen Konsolen-Ausgaben.  
**Erwartetes Ergebnis / Soll-Zustand:** Du hast ein lauffähiges Node.js-Skript, das Such-, Sortier- und Stack-Funktionalität in einem realistischen Beispiel kombiniert.

## Erweiterungsaufgaben

### Erweiterungsaufgabe 1: Suche nach Statuscode

**Ziel:** Du erweiterst die lineare Suche für mehrere Treffer.  
**Arbeitsauftrag:** Schreibe eine Funktion `findRequestsByStatus(requests, status)`, die alle Requests mit einem bestimmten Statuscode zurückgibt, z. B. `200`, `404` oder `500`. Gib die Treffer übersichtlich aus und zeige auch an, wenn es keine passenden Einträge gibt.  
**Erwartetes Ergebnis / Soll-Zustand:** Du kannst mehrere passende Elemente in einem Array linear finden und sinnvoll darstellen.

### Erweiterungsaufgabe 2: Bubble Sort absteigend oder mehrfach verwendbar

**Ziel:** Du machst deine Sortierfunktion flexibler.  
**Arbeitsauftrag:** Passe deine Bubble-Sort-Funktion so an, dass du wahlweise aufsteigend oder absteigend sortieren kannst. Optional kannst du zusätzlich einen Parameter einbauen, mit dem du nach verschiedenen Feldern sortierst, z. B. `durationMs` oder `status`.  
**Erwartetes Ergebnis / Soll-Zustand:** Deine Sortierung ist wiederverwendbar und nicht nur auf einen festen Fall beschränkt.

### Erweiterungsaufgabe 3: Stack für Undo von Request-Markierungen

**Ziel:** Du nutzt den Stack in einem noch realistischeren Anwendungsszenario.  
**Arbeitsauftrag:** Ergänze deine Requests um ein Feld wie `reviewed: false`. Schreibe eine Funktion, mit der du einen Request als geprüft markierst und den vorherigen Zustand auf einem Stack speicherst. Implementiere anschließend eine Undo-Funktion, die den letzten Zustand wiederherstellt.  
**Erwartetes Ergebnis / Soll-Zustand:** Du verwendest den Stack sinnvoll für eine Rückgängig-Funktion und kannst Änderungen am Datenbestand zurückrollen.

## Wichtige Hinweise

- Arbeite in kleinen, testbaren Schritten.
- Starte dein Skript regelmäßig mit `node dateiname.js`.
- Nutze `console.log()` oder `console.table()`, um Zwischenergebnisse sichtbar zu machen.
- Achte auf sprechende Funktionsnamen und saubere Einrückung.
- Wenn du an einer Stelle nicht weiterkommst, vereinfache zuerst die Daten oder teste mit kleineren Arrays.
- Überschreibe Daten nicht unabsichtlich, wenn du sortierst oder Elemente entfernst.

## Reflexionsfragen

- Wann reicht ein Array für dein Problem aus?
- Wann ist ein Stack die bessere Wahl?
- Was passiert bei der linearen Suche, wenn das Array sehr groß wird?
- Warum ist Bubble Sort leicht zu verstehen, aber für große Datenmengen oft ungeeignet?
- An welcher Stelle in deinem Skript siehst du den stärksten Praxisbezug zu einem Backend-Projekt?

---