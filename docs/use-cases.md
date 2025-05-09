# Use Cases
🔵: Wird dran gearbeite
🟢: Umgesetzt
🟠: Optionl


## 1. Virtueller Studienassistent 🔵

**Zielgruppe**: Studierende  
**Need**: Studierende möchten individuelle Fragen mit einem Avatar klären können.  
**Funktion**: Der Avatar beantwortet Fragen zu Vorlesungen, Inhalten, Terminen und Prüfungen.  
**Ausgestaltung**:  
- Plattform mit Kursauswahl  
- Start eines Gesprächs mit einem virtuellen Avatar  
- Antworten basieren auf Kursdaten  

---

## 2. Virtuelle Lernhelfer

**Zielgruppe**: Studierende  
**Need**: Individuelle Lernmaterialien und Lernpläne  
**Funktion**: Der Avatar erstellt passende Aufgaben und Probeklausuren  
**Ausgestaltung**:  
- Dynamische Aufgaben basierend auf Vorlesungsinhalten  
- Abschluss mit automatisch generierter Probeklausur  

**Risiken**: Falsche Aufgaben oder Lösungen können zu Fehlvorstellungen führen  
**MVP-Relevanz**: MVP v2

---

## 3. Spracheinstellung

**Zielgruppe**: Internationale Studierende  
**Need**: Inhalte müssen in verschiedenen Sprachen verfügbar sein  
**Funktion**: Möglichkeit zur Sprachauswahl  
**Ausgestaltung**:  
- Drop-down-Menü zur Auswahl der Sprache  
- Sprachen: Deutsch und Englisch  

**MVP-Relevanz**: Optional

---

## 4. Quellenverweis

**Zielgruppe**: Studierende und Professoren  
**Need**: Antworten des Avatars müssen nachvollziehbar und belegbar sein  
**Funktion**: Anzeige von Quellen bei datengestützten Aussagen  
**Ausgestaltung**:  
- In jeder relevanten Antwort wird ein Informationssymbol angezeigt  
- Beim Öffnen erscheinen die verwendeten Quellen  

**MVP-Relevanz**: Optional

---

## 5. Avatar-Generierung 🔵

**Zielgruppe**: Professoren  
**Need**: Professoren möchten einen personalisierten Avatar für ihr Modul erstellen  
**Funktion**: Erstellung eines digitalen Abbilds über ein Interface  
**Ausgestaltung**:  
- Upload von Bildern, 3D-Scans und Audiodateien  
- Generierung eines individuellen Avatars  

**MVP-Relevanz**: MVP v1

---

## 6. Raumgestaltung 🔵

**Zielgruppe**: Professoren  
**Need**: Kursspezifische Wissensräume sollen individuell gestaltet werden können  
**Funktion**: Generierung separater Rauminstanzen mit spezifischem Wissenskontext  
**Ausgestaltung**:  
- Administrationsseite zur Erstellung von Kursräumen  
- Konfiguration der Inhalte und des Kontextes für den Avatar  

**MVP-Relevanz**: MVP v1 (zunächst ein Raum)

---

## 7. Skills festlegen

**Zielgruppe**: Professoren  
**Need**: Kontrolle über die Funktionen des Avatars  
**Funktion**: Aktivieren oder Deaktivieren einzelner Fähigkeiten  
**Ausgestaltung**:  
- Liste mit ein- und ausschaltbaren Funktionen  

| Skill                 | Beschreibung                                                            |
|-----------------------|-------------------------------------------------------------------------|
| Vorlesungswissen      | Avatar beantwortet Fragen zur Vorlesung anhand hochgeladener Daten      |🔵
| Termine               | Avatar nennt relevante Termine                                           |🟠
| Aufgaben generieren   | Aufgaben basierend auf Vorlesungsdaten                                  |🟠
| Lernplan erstellen    | Lernplan mit Aufgaben und Terminen                                      |🟠
| Ansprechpartner finden| Bei zu komplexen Fragen verweist der Avatar an zuständige Personen      |🟠
| Notifikationen senden | Der Avatar kann aktive Benachrichtigungen auslösen                      |🟠

---

## 8. Accounts und Rechteverwaltung

**Zielgruppe**: Studierende und Professoren  
**Need**: Unterschiedliche Funktionen je nach Nutzerrolle  
**Funktion**: Login- und Registrierungssystem mit Rollensteuerung  
**Ausgestaltung**:  
- Login-/Registrierungsseite  
- Rollenzuweisung (Student / Professor) mit unterschiedlichen Rechten  


---

## MVP-Planung

## MVP v1 – Technische Machbarkeit

In der ersten Version des Systems steht die **technische Machbarkeit** im Vordergrund. Ziel ist es, eine minimale, aber funktionierende End-to-End-Plattform zu realisieren, auf der sowohl Professoren als auch Studierende erste Kernfunktionen nutzen können.

### Funktionen für Professoren

Professoren sollen die Möglichkeit haben:

- Einen eigenen Avatar zu erstellen, der als digitales Abbild ihrer Person fungiert.
- Mindestens eine Wissensquelle (z. B. ein PDF, Foliensatz oder Text) pro Raum zu hinterlegen, um dem Avatar eine Grundlage für Antworten zu geben.
- Unterschiedliche virtuelle Räume (Kurse) zu eröffnen, in denen jeweils ein eigener Avatar mit spezifischem Wissen agiert.

### Funktionen für Studierende

Studierende sollen die Möglichkeit haben:

- Eine einfache Benutzeroberfläche (UI) aufzurufen, über die sie verfügbare Kurse auswählen können.
- Mit dem Avatar innerhalb eines Kurses zu interagieren, wobei der Avatar nur auf das vom Professor bereitgestellte Wissen in diesem Raum zugreifen kann.


## MVP v2

- Lernhelfer (Use Case 2)  
- Termin-Integration  
- Skill-Steuerung  
- Lernplan-Erstellung  
- Aufgaben-Generierung  
- Weitere Avatar-Skills
