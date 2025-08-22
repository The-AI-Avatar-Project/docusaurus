# Technical Debt


| Titel                    | Beschreibung                                                                                                                                       | Bereich                 |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| Load-Balancer            | Es besteht derzeit keine Skalierung, weshalb nur ein einzelner Nutzer eine ansatzweise flüssige Erfahrung hat.                                    | Backend – Videopipeline  |
| Unverschlüsselte Datenbank | Backend-Daten liegen unverschlüsselt in der PostgreSQL-Datenbank vor.                                                                            | Backend – PostgreSQL     |
| Keycloak-Abhängigkeit    | Die Businesslogik bezüglich Gruppen, Kursen usw. wird vollständig über Keycloak abgebildet, was einen Wechsel des Identitätsmanagements stark erschwert. | Backend – Keycloak       |
| Lizenzpflichtige Audio- und Video-Generierung | Wav2Lip und Coqui/XTTS v2 unterliegen eigenen Lizenzbestimmungen, die für die kommerzielle Nutzung eingeholt werden müssen.     | Video-/Audio-Pipeline    |
| Fehlendes Request-Limiting | Es fehlt ein Schutz vor zu vielen Anfragen pro Nutzer. Dadurch können Ressourcen wie das OpenAI-Kontingent schnell verbraucht oder das System überlastet werden. | Backend – LLM|
| API-Ketten-Komplexität   | Jeder Service ist separat containerisiert und stellt eine eigene API bereit. Zwischen Backend und KI-Services existieren verschachtelte API-Aufrufe (APIs auf APIs), was die Gesamtkomplexität erhöht und potenzielle Fehlerquellen vervielfacht. | Architektur              |