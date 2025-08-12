# Meeting-log

### 14.04.2025 – Kick-off-Meeting
- Erstes Projekttreffen
- Einführung durch Herrn Gedikli zu KI-Assistenten und Avataren
- Entscheidung zur Entwicklung erster Use Cases

### 21.04.2025 – Team-Arbeitstreffen
- Besprechung der Projektideen und Zieldefinition
- Bildung von Arbeitsgruppen:
  - **Videofeed**: Andreas & Leon  
  - **Frontend**: Okan & Silas  
  - **TTS / STT**: Doriane & Stella  
  - **Backend**: Nils & Paul
- Aufgabe: Technischen ersten aufschlag erarbeiten. Was für tools wie nutzen?

### 01.05.2025 – Team-Arbeitstreffen
- Vorstellung der finalen Use Cases
- Präsentation erster Teilergebnisse durch alle Teams
    - **Videofeed**: Erstaufschlag unterschiedlicher tootl mimictalk, sadtalker, 
    - **Frontend**: Erste UI idee 
    - **TTS / STT**: Unterschidelichste TTS und STT services
    - **Backend**: Erster python backendansatz mit whisper
- Outcomes:
    - **Videofeed**: Zu langsam
    - **Frontend**: Silas Idee angenommen mit zentriertem avatar
    - **TTS / STT**: STT wird mit whisper local hosted umgesetzt
    - **Backend**: Dsikussions punkt eröffnet bezüglich Conatiner ansatz oder monolyth ansatz
- ToDos: 
    - **Videofeed**: Weiter arbeiten an alternativen wie geneface++, anderen konzepten, recherche dritanbieter
    - **Frontend**: Erste implementierung des UIs
    - **TTS / STT**: TTS weiter recherche für lokal hostbare systeme
    - **Backend**: Einarbeitung in anbindung eines LLMs

### 05.05.2025 – Vorstellung beim Professor
- Präsentation der bisherigen Ergebnisse
- Entscheidung zur Nutzung der OpenAI API (Budget: 50 €)
- findbar hier [Passwort-Datei herunterladen](\/downloads\AvatarProjekt.kdbx) 
- Die heruntergeladene Datei ist im KeePass-Format (.kdbx) und kann mit dem kostenlosen Passwortmanager [KeePass](https://keepass.info/download.html) geöffnet werden.
- Python als backend wurd revidier und auf Java geeinigt. 
- Docusaurus als project seite festgelegt

### 09.05.2025 - Team-Arbeitstreffen
- Präsentation der bisherigen Ergebnisse
    - **Videofeed**: MimicTalk und SadTalker wurden ausgeschlossen. Drei neue Ansätze sind aktuell in Arbeit:
        1. **Minimalansatz**: Steuerung über Lautstärkepegel und zwei festgelegte Frames (z. B. neutral und sprechend).
        2. **Phonem-basierter Ansatz**: Nutzung von Phoneminformationen für differenziertere Mimik.
        3. **wav2Lip**: Visuell realistischere Lippenbewegungssynchronisation (wird derzeit getestet).
    - **Frontend**: Intensivierter Austausch und Planung zur weiteren Umsetzung.
    - **TTS / STT**: Weitere lokal laufende TTS-Projekte wurden gesammelt und dokumentiert.
    - **Backend**: Erste Experimente mit ChromaDB und LangChain durchgeführt.
- ToDos: 
    - **Videofeed**: wav2Lip wird noch bis zu 7 Tage getestet. Falls kein zufriedenstellendes Ergebnis, erfolgt die Weiterarbeit an den beiden Minimalansätzen.
    - **Frontend**: Erste Umsetzung des UI geplant (möglicherweise mit PrimeNG-Framework, noch offen); zusätzlich ist mindestens eine OpenAI-Chat-Verbindung vorgesehen, um das Mocken von Textinhalten zu ermöglichen.
    - **TTS / STT**: Verschiedene TTS Systeme testweise lauffähig machen und Feedback einholen, welches alle Anforderungen erfüllt.
    - **Backend**: Umsetzung des ersten Backend-Abschnitts: Datenbank, Google Text-to-Speech, Whisper. (Google Text-to-Speech zum mocken keine finale entscheidung)
- Eröffnete disukssuion:
    - Das Thema Nutzer-Login wurde angeschnitten. Perspektivisch wird in Betracht gezogen, später eventuell Keycloak einzusetzen – alternativ wird geprüft, inwiefern die vorhandenen Spring Boot-Funktionalitäten dafür ausreichen.

### 16.05.2025 – Team-Arbeitstreffen
- Die Teams arbeiten produktiv weiter:
    - **Videofeed**:  
        - Leon setzt den Minimalansatz technisch um (Lautstärke + zwei Frames).  
        - Andreas arbeitet an einer streambaren Variante von wav2Lip.  
    - **Frontend**:  
        - Erster UI-Prototyp erfolgreich umgesetzt.  
        - Direkte Anbindung an OpenAI ChatGPT und ElevenLabs TTS integriert.  
    - **TTS / STT**:  
        - Weitere Recherchearbeit zu lokal ausführbaren TTS-Systemen.  
    - **Backend**:  
        - Präsentation des internen Workflows „**RAG**“ (Retreval-Augmented Generation).  
        - Vorstellung von **Spring AI** als Alternative zu LangChain.  
        - **PGVector** als PostgreSQL-basierte Vektor-Datenbankalternative zu ChromaDB diskutiert.  
- ToDos:
    - **Videofeed**:  
        - Leon und Nils integrieren den Minimalansatz ins Backend.  
        - Andreas arbeitet weiter am Streamingansatz mit wav2Lip.  
    - **TTS / STT**:  
        - Fokus auf Coqui: Erste lauffähige lokale Instanz soll erstellt werden.  
    - **Frontend**:  
        - Git-Repository anlegen.  
        - Erste Anbindungen zum Backend implementieren (abhängig vom Fortschritt des Backend-Teams).  
    - **Backend**:
        - Nils stellt Endpoints bereit, um über Sprache und Chat mit dem Chatbot zu interagieren.

### 19.05.2025 - Vorstellung beim Professor
- Jedes Teammitglied hat den eigenen Fortschritt vorgestellt.
- Die Evaluationsstrategie im Hinblick auf die Kosten wurde präsentiert:
    - Professoren sollen befragt werden, wie viele Routinefragen sie üblicherweise erhalten und wie lange die Bearbeitung durchschnittlich dauert.
    - Daraus sollen die potenziellen Einsparungen gegenüber den laufenden Systemkosten pro Jahr bzw. Semester berechnet werden.
- Daraus sollen die potenziellen Einsparungen gegenüber den laufenden Systemkosten pro Jahr bzw. Semester berechnet werden. 
    -Dies ist jedoch aufwendiger umzusetzen und könnte die Entwicklungszeit entsprechend verlängern. Eine Entscheidung dazu steht noch aus (TBD).
- Potenzielle Probleme im Zusammenhang mit Voice Cloning wurden thematisiert (siehe Riklog vom 16.05.2025):
    - Der Professor erkundigte sich nach einer möglichen Kostenübernahme für die Nutzung von ElevenLabs.
    - Bevorzugt wurde jedoch von ihm eine eigenständig gehostete Lösung.
- Die Frage, wie man das Budget bzw. die Token-Nutzung bei OpenAI beobachten kann, wurde gestellt. Der Professor wird diesbezüglich Rücksprache mit der IT halten.


Es wurde die Evaluationsstrategie auf kosten vorgestellt (Profs fragen wieviele routine fragen sioe bekommen wie lange es dauert eine abzuarbeiten kosten berechen vs laufende kosten des systems pro jahr / semesters)
Einwurf das man irgendwie noch die qualität der antworten analysieren sollte tbd da dies aufwendoiger ist und dementsprechend die entwicklungszeit reduziert werden würde. 
Hingewiesen auf potenzielle probleme mit voicecloning wurden angesprochen (Riklog 16.05.2025) -> Professor fragt nach bezüglich kosten übernahme bei Elevenlabs präferert allerdings eine eigen gehostste umsetzung
Frage tokennutzung wie können wir die kosten ermitteln wurde angesprochen 

### 23.05.2025 – Team-Arbeitstreffen
- Die Teams arbeiten produktiv weiter:
    - **Videofeed**:  
        - Leon keine großen änderungen an dem minimal video feed ansatz
        - Andreas hat vorerst den Wav2Lip-Ansatz abgeschlossen. Für den V2-Ansatz hängt die weitere Entwicklung von den Ergebnissen von Leon ab.
    - **Frontend**:  
        - Zwei Mockups wurden von Silas und Okan erstellt. Es wurde entschieden, den Ansatz von Silas zu übernehmen, da er bereits erfolgreich die Verbindung zum Backend umsetzen konnte.
        - Einschäzung Okans war es das der quellcode vernüftig umgesetzt ist von Silas und das keine größeren schwieigkeiten bei der zusammenarbeit entsehen sollten.
    - **TTS / STT**:  
        - Erste Erfolge beim Testen von Coqui und OpenVoice.
    - **Backend**:  
        - Die Umsetzung des "Daten hinterlegen"-Features sowie das Abrufen via RAG ist erfolgreich eingebaut.
- ToDos:
    - **Videofeed**:  
        - Leon arbeitet mit dem Backend-Team daran, einen Live-Feed möglich zu machen.
        - Andreas wechselt in das neue Arbeitspaket "Keycloak-Umsetzung".
    - **TTS / STT**:  
        - Coqui und OpenVoice in Container einarbeiten, um sie später im Backend nutzbar zu machen.
    - **Frontend**:  
        - Videofeed in die UI einbinden.
        - Mockup planen, wie Referenzen auf Dokumente dargestellt werden sollen.
        - Evaluieren, wie man das Mikrofon vom Browser aus ansteuern kann.
        - Settings planen und erste Implementierung vornehmen, um Dozenten und Studenten (später) unterschiedliche Funktionen bereitzustellen (z. B. Raum anlegen, Sprache auswählen, Räume für Studenten freigeben etc.).
    - **Backend**:
        - Videofeed mit Leon einbinden.
        - Endpoint erstellen, um Professoren-Profile anzulegen (Name + Bild).

### 30.05.2025 – Ausgefallen da zu viele abwesend waren
- Seperate mini updates an Anderas nachträglich eingegangen
- **Videofeed**: Leons minimal ansatz ist präsentaionsreif
                Andreas Wav2Lip ansatz ist streambar
                Übereingekommen das ab hier an der einbiundung von wav2lip gearbeitet wird
- **TTS / STT**:  Dorane und Stelle arbeiten an docker files für coqui un dopenvoice
- **Frontend** : Silas  und Okan konnten erfolgreich den Videostream und die änderung auf Sockets einbuinden ins frontend
- **Backend**: Soweit fortgeschritten das jetzt langsam die einbindung vin keycloak backend seitig eingeführt werden kann


### 19.05.2025 - Vorstellung beim Professor
- Jedes Teammitglied hat den eigenen Fortschritt vorgestellt.
- Doing vom Prof einlesen in den EU AI act 

### Anpassung der aufgaben teilung
## TTS
- OpenVoice: Stelle & Nils 
- Coqui: Andreas & Doriane 

- **Ziel**: Bereitstellung von:
  - einem Endpoint zur **generierung eines voice embeddings / clones** (parameter: ID, refernz.wav)
  - einem Endpoint zur **Auswahl einer Stimme** +  **Text-zu-Sprache-Ausgabe**. rückgabe einer wav datei (streaming erstmal zweitrangig da aussteht ob wav2lip in-coming streaming am ende umsetzen kann)



## Frontend
### Leon, Silas & Okan
- Aufgabenverteilung erfolgt im Sub-Team selbstorganisiert.
- **Ziele**:
  - Integration des **Mikrofons**
  - Einstellungen realisieren so weit wie möglich (so viel implementieren wie möglich, so wenig mockup wie nötig)
  - Planung wie ein Onboarding / setup prozess für neue nutzer Profs aussehen könnte

## Backend
### Paul
- Umsetzung eines Endpoints zum **Anlegen von Profilordnern**:
  - Struktur: `/profile/<Keycloak-User-ID>/`
  - Inhalte:
    - Referenzvideos oder Bilddaten für den videofeed.
    - Später: Embeddings zur Stimmanpassung.

## Frontend / Backend
### Andreas, Nils
- KeyCloak verifikation bei request zum laufen bekommen



## 13.06.2025 – Team-Arbeitstreffen

Die Teams präsentierten ihre Zwischenergebnisse und es erfolgte eine neue Arbeitsteilung:

# TTS / STT  
- Stella & Nils OpenVoice ergebniss: Nicht funkunell nutzbar für dieses Projekt aufgund von mangelnden Sprach optionen.  
- Andreas & Dorinae: Coqui wurde erfolgreich mit einer api ansteuerbar gestaltet und an Nils weitergegeben für das backend.
# Videofeed  
- Wav2Lip wurde erfolgreich mit einer api ansteuerbar gestaltet und an Nils weitergegeben für das backend.

# Frontend (Team: Okan, Silas & Leon)  
- Silas präsentierte die überarbeitete Hauptseite welche nun jahre / Professoren / Kurse strukturiert darstellt.
- Okan stellte die Einstellungsseite vor, umgesetzt mit PrimeNG.  
  - Entscheidung: Hauptseite bleibt Custom CSS, alle weiteren Komponenten werden mit PrimeNG umgesetzt / angepasst.  
- Leon demonstrierte die funktionale Mikrofonanbindung im Frontend (derzeit noch via externer API).

# Backend  
- Nils hat Wav2Lip und Coqui im Backend integriert.  
- Die durchgehende Sprach-/Videopipeline ist fast vollständig funktionsfähig.  
- Erste Schritte nuzung von Keycloak sind erfolgt.

# ToDos:

**Andreas**
- Setup-Skripte für KeyCloak anpassen (Struktur Jahr/Prof Name/ Kursname und das setzen von icon tags)
- Unterstützung bei der Frontend-Keycloak-Integration.

**Silas**
- Integration seiner Hauptseite mit Keycloak.
- KeyCloak token nutzen und verarbeiten um Gruppen zugehörigkeit einzulesen. 

**Okan**
- Umsetzung der Einstellungen-UI mit PrimeNG.
- Konzeption des Prozesses für Raum erstellung, Nutzer einladen, Daten hinterlegen (Mockup endpoints nutzen aber implementieren mit PrimeNG)
- Konzeption des Prozesses Profil anlegen (Professor) (Bild speichern , referenz stimme hochladen, (Mockup endpoints nutzen aber implementieren mit PrimeNG)).
- Zusammenarbeit mit Nils zur Definition der Backend-Endpunkte für Profil- und Raumgenerierung (Falls Nils die Kapas dafür hat diese woche).

**Leon**
- Weiterentwicklung der Mikrofonanbindung im Frontend.
- Integration mit dem echten Backend zur Sprachverarbeitung.

**Nils**
- Verfeinerung der Backend-Endpunkte für Audio- und Videoverarbeitung.
- Überarbeitung der README.
- Nach Abschluss der obigen Aufgaben: Zusammenarbeit mit Okan zur Umsetzung der Profil- und Raum-Endpunkte.

**Doriane & Stella**
- Analyse des European AI Act:
  - Welche Kennzeichnungspflichten gelten für KI-generierte Videos?
  - Reicht ein Hinweis in der Fußnote oder ist ein Watermark erforderlich?

## 20.06.2025 – Team-Arbeitstreffen

Die Teams präsentierten ihre aktuellen Arbeitsstände und planten die nächsten Schritte:


# ToDos:

**Andreas**  
  - Der bestehende Coqui-TTS-Teil wird überarbeitet, um eine **streambare Variante** zu ermöglichen.  
  - Wahrscheinlich wird das bisherige Coqui-Framework durch einen direkten Zugriff auf **XTTSv2** ersetzt.

**Leon**  
  - Untersuchung zur **Ansteuerung von OpenAIs Bildgenerator**, mit dem Ziel, **konsistente Bilder** zu generieren.  
  - Weiterentwicklung des **Minimalansatzes**: Es wird geprüft, wie zusätzliche **Ausdrucksformen**  integriert werden können.

**Okan**  
  - Weiterarbeit an der Umsetzung der UI mit **PrimeNG**.  
  - **Ziel bis nächsten Freitag**:
    - **Raumerstellung** durch Professoren soweit wie möglich umgesetzt:
        - **Mindestens**: Raum mit Namen anlegen und Auswahl aller Studierenden anzeigen für den "Studenten zu Kurs hinzufügen" vorgang.
        - **Zusätzlich**: Daten-Hochladen-Funktion als **Mockup** integrieren und **alle hochgeladenen Daten anzeigen**.

**Silas**
    - Erste schritten zur multilingualen webseite für eine mvp umsetzung zu nächst deutsch und englisch

**Nils & Paul**  
  - Weiterentwicklung der **Endpoints zur Raumerstellung** (Raum anlegen + Studenten auflisten).  
  - Endpoint zum Downloaden von referenzen und generell ermöglichen die referenzen anzuegeben. 

**Doriane & Stella**  
  - Entscheidung, **wer als Ansprechpartner:in für den EU AI Act** im Projekt fungiert.  
  - Recherche von **Quellen**, die klären:
    - Ob **Watermarks** in KI-generierten Videos verpflichtend sind.
    - Oder ob ein **Hinweis im Footer oder unter dem Video ausreichend** ist.



## 27.06.2025 – Team-Arbeitstreffen

Die Teams updatete sich via WhatsApp wer wie weit ist.

# ToDos

**Andreas**
- Audio- und Video-Pipeline Code aufräumen
- Meeting mit dem Backend-Team zur Anbindung der neuen Video-Pipeline


**Leon**

- Drei Themen ausdenken, die komplex genug sind, um sie in einer Lektion zu lernen  
  **Anforderungen:**  
  1. Muss für „0815“-Menschen neu sein – also etwas, das man nicht kennt  
  2. Benötigt keine / wenig visuellen Erklärungen
  3. Einfach per Multiple-Choice-Test abfragbar

**Okan**
- **Ziel bis nächsten Freitag:**
  - **Raumerstellung anpassen**:
    - Avatar hinterlegen/anpassen  
      → Eigener Menüpunkt oder bei Zeitmangel: aktuelle Version mit „Skip“-Button
    - Upload von Materialien im Kurs  
      → Nur **PDF** zulassen
    - Raum-Icon festlegen  
      → Im Raum Erstellungsprozess auswählbar (In kooperation mit Silas der hat sich das ganze ausgedacht)
    - Anbindung an **Keycloak**  
      → Gemockte Daten entfernen
    -  Anbindung an **Backend**  
      → Nutzerliste aus dem Backend abrufen

**Silas**
- Okan **unterstützen**, wo möglich
- Referenzen im chat vernünftig anzeigen
- Spracheinstellung vorbereiten  
  → Es reicht aktuell, `"de"` oder `"en"` zu senden (Backend-Endpoint folgt)


**Nils & Paul**

- Meeting mit andres bezüglich video audio pipeline
- Endpoint um nutzer in Kurs einzutragen
- Endpoint um sprache zu hinterllegen


**Doriane & Stella**

- Datenschutzerklärung verfassen  
  → Inhalt:
  1. Datenverarbeitung durch **OpenAI**
  2. Speicherung von **Testergebnissen** zur Evaluation


## 04.07.2025 – Team-Arbeitstreffen

Die Teams präsentierten ihre aktuellen Arbeitsstände und planten die nächsten Schritte:

# ToDos

**Nils**  
- Weitere Kleinigkeiten an der Audio- und Video-Pipeline umsetzen

**Okan**  
- Abschluss des Raumerstellungs- und Avatar-Anlegeprozesses

**Silas**  
- Einbindung der neuen Audio- und Video-Pipeline

**Doriane & Stella**  
- Bewertung von Projektrisiken in Bezug auf den Datenschutz

## 21.07.2025 – Vorstellung beim Professor
Allgemein wenig updates aufgrund von Prüfungsphase 

** Andreas **
- Angefangen abschließende Dokumentaion zu schreiben 

** Silas **
- Kleinigkeiten im frontend

** Okan **
- Fast fertig mit frontend nur noch endpoin anstuern um refernz audio hochzuladen

** Nils ** 
- Backend soweit abgeschlossen 

** Doriane Stelle **
- Datenschutzerköärung geschrieben und Risiko klasse definiert

ToDo

** Nils **
- Zugang zu server beantragen

** Silas **
- Videopipeline anbinden 

** Okan **
- Audio referez hochladbar machen

** Andreas ** 
-Technical debt und Mermaid diagramme anfangen
- Professoren anschreiben wegen FAQ - emails und wie der zeitaufwand ist


---
