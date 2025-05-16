# Videofeed

## Anforderungen

Der Videofeed soll folgende Kriterien erfüllen:

1. Die Gestik des Charakters soll zur gesprochenen Sprache passen und eine gesprächsähnliche Interaktion ermöglichen.  
2. Der Charakter soll dem Dozenten oder der Dozentin optisch ähnlich oder identisch sein.  
3. Die Generierung des Avatars soll durch ein zu Beginn hochgeladenes Bild erfolgen.  
4. Sprache und Animation sollen dynamisch erzeugt werden – kein vorgefertigtes oder loopendes Video.

## Evaluierte Ansätze

Wir haben sechs Ansätze untersucht, um den Videofeed technisch umzusetzen:

### MimicTalk

![MimicTalk Diagramm](/video-feed/mimictalk.drawio.png)

MimicTalk erzeugt ein realistisches Video allein auf Basis eines Bildes und einer Audiodatei. Die Ergebnisse wirken sehr echt und überzeugend.

**Nachteil:**  
Die Generierung ist extrem zeitaufwendig – etwa 300 Sekunden Rechenzeit für 10 Sekunden Audio.

**Fazit:**  
**Abgelehnt** – zu hohe Latenzzeit.

---

### SadTalker

![SadTalker Diagramm](/video-feed/sadtalker.drawio.png)

SadTalker nutzt ein ähnliches Verfahren wie MimicTalk, benötigt aber weniger Rechenleistung bei geringerer Qualität.

**Nachteil:**  
Auch hier ist die Generierung zu langsam – ca. 1560 Sekunden für 10 Sekunden Audio.

**Fazit:**  
**Abgelehnt** – zu hohe Latenzzeit.

---

### GeneFace++

![GeneFace++ Diagramm](/video-feed/genefaceplusplus.drawio.png)

GeneFace++ verspricht Echtzeit-Rendering basierend auf dem MimicTalk-Prinzip.

**Nachteil:**  
In unserer Docker-Umgebung war eine funktionierende Implementierung nicht möglich.

**Fazit:**  
**Abgelehnt** – technische Umsetzung derzeit nicht machbar.

---

### Wave2Lip-Ansatz

![Wave2Lip Diagramm](/video-feed/wave2lip-ansatz.drawio.png)

Ein hybrider Ansatz: Ein stummes Video (z. B. mit MimicTalk) mit Gestik wird vorab erstellt. Danach wird mit Wave2Lip die Lippenbewegung anhand der Audiodatei ergänzt.

**Fazit:**  
**In Prüfung** – ...

---

### Minimal-Ansatz

![Minimal-Ansatz Diagramm](/video-feed/minimal-ansatz.drawio.png)

Ein bewusst einfacher Ansatz, der das Mindestmaß an Funktionalität umsetzt. Der Avatar besitzt nur zwei Mundstellungen: offen und geschlossen. Der Wechsel zwischen diesen Zuständen wird dynamisch anhand des Lautstärkepegels der Audiodatei gesteuert.

**Fazit:**  
**In Umsetzung**

---

### Phonem-Ansatz

![Phonem-Ansatz Diagramm](/video-feed/phonem-ansatz.drawio.png)

Bei diesem Ansatz wird der Avatar auf Basis von Phonem-Zeitstempeln animiert. Zu jedem Phonem wird das passende Bild mit entsprechender Mundstellung ausgewählt und in chronologischer Reihenfolge zu einem Video zusammengeschnitten.

**Fazit:**  
**TBD**



---
