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


---
