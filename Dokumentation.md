# Dokumentation LA1303
## Passwort-Manager-Projekt 

Angelov, Bajramovic, Jashari, Marku



| Datum      | Version | Zusammenfassung                                                                       |
|------------|---------|---------------------------------------------------------------------------------------|
| 12.01.2024  | 0.0.1   | Projektinitiierung und erste Diskussion über Verschlüsselungsmethoden.                 |
| 19.01.2024  | 0.0.2   | Beginn der Programmierung mit Grundfunktionalitäten.                                   |
| 26.01.2024  | 0.0.3   | Implementierung der Datenbank zur Speicherung der Passwörter.                          |
| 02.02.2024  | 0.0.4   | Implementierung von Verschlüsselungsfunktionen für die sichere Speicherung von Daten. |
| 23.02.2024  | 0.0.5   | Die letzten Feinschliffe werden dem Projekt gegeben und der Portfolioeintrag wird geschrieben.                   |

## 1. Informieren

### 1.1 Ihr Projekt

Das Ziel dieses Projekts ist die Entwicklung eines einfachen Passwort-Managers, der es Benutzern ermöglicht, ihre Passwörter sicher zu speichern, anzuzeigen und zu verwalten. Der Passwort-Manager soll eine einfache Konsolenanwendung sein, die die grundlegenden Funktionen eines Passwort-Managers, wie das Hinzufügen, Anzeigen und Löschen von Passwörtern, unterstützt. Zusätzlich wird eine Verschlüsselungsfunktion implementiert, um die Sicherheit der gespeicherten Passwörter zu gewährleisten.


### 1.2 User Stories

| US-Nr. | Verbindlichkeit | Typ         | Beschreibung                                                                                          |
|--------|-----------------|-------------|-------------------------------------------------------------------------------------------------------|
| 1      | Muss            | Funktional  | Als Benutzer möchte ich beim Start des Programms wählen können, ob ich die Passwörter anschauen  oder hinzufügen möchte. |
| 2      | Muss            | Funktional  | Als Benutzer möchte ich den Namen der Website angeben können, um zu wissen, zu welcher Anwendung das Passwort gehört.  |
| 3      | Muss            | Funktional  | Als Benutzer möchte ich das Passwort eingeben können, damit es zusammen mit der Website und der ID gespeichert wird. |
| 4      | Muss            | Funktional  | Als Benutzer möchte ich die Möglichkeit haben, mein Passwort vor der Speicherung zu verschlüsseln, um die Sicherheit meiner Daten zu erhöhen. |
| 5      | Muss            | Funktional  | Als Benutzer möchte ich eine Liste aller gespeicherten Passwörter einsehen können, um einen Überblick zu erhalten.  |
| 6      | Muss            | Funktional  | Als Benutzer möchte ich die Möglichkeit haben, ein gespeichertes Passwort zu löschen, um meine Daten aktuell zu halten. |
| 7      | Kann            | Funktional  | Als Benutzer möchte ich, dass das Programm Fehlermeldungen angemessen behandelt, um die Benutzererfahrung zu verbessern.  |
| 8     | Muss            | Funktional  | Als Benutzer möchte ich, dass meine Daten nach dem Beenden des Programms gespeichert bleiben und bei erneutem Start verfügbar sind. |
| 9     | Kann            | Funktional  | Als Benutzer erwarte ich eine benutzerfreundliche Oberfläche, die die Nutzung des Programms intuitiv und einfach macht. |



### 1.3 Testfälle

| TC-Nr. | Ausgangslage                                 | Eingabe                  | Erwartete Ausgabe                                                                                                         |
|--------|----------------------------------------------|--------------------------|-------------------------------------------------------|
| 1.0   | Programm gestartet, Hauptmenü wird angezeigt | "1"                      | Weiterleitung zum Hinzufügen-Menü; Aufforderung zur Eingabe des Namens der Website, für die das Passwort gespeichert werden soll: "Website: " |
| 2.0    | Website-Namen eingegeben                     | [Website-Name]           | Aufforderung zur Eingabe des Benutzernamens: "Username: " |
| 3.0    | Passwort eingegeben                          | [Passwort]               | Bestätigung, dass der eigene Passwort gespeichert wurde; Rückkehr zum Hauptmenü        |
| 4.0    | Verschlüsselungsauswahl getroffen            | "2"                      | Bestätigung, dass das Passwort automatisch verschlüsselt wurde; Rückkehr zum Hauptmenü                   |
| 5.0    | Zurück im Hauptmenü                          | "2"                      | Liste aller gespeicherten Passwörter anzeigen |
| 6.0    | Löschen eines Passworts       | "Beliebige ID Nummer"                      | Passwort wurde gelöscht   |
| 7.0 | Im Hauptmenü | "5" |Es erscheint eine rote Fehlermeldung und man kann daraufhin eine weitere Eingabe machen. |
| 8.0 | Im Hauptmenü | "4" | Das Programm wird beendet und Daten werden gespeichert. |
| 9.0 | Programm wieder starten; im Hauptmenü | "2" | Vorherige gespeicherte Daten werden hervorgehoben. |



### 1.4 Diagramme
![Hauptprogramm 1](https://github.com/denisjashari54/LA1303/assets/112430127/82f61273-bd01-439a-9718-be3ffa20d551)

## 2 Planen

| AP-Nr. | Frist      | Zuständig   | Beschreibung                                                    | Geplante Zeit |
|--------|------------|-------------|-----------------------------------------------------------------|---------------|
| 1.A    | 12.01.2024 | Alle        | Informationssammlung und -austausch über Projektziele.          | 240'|
| 2.A    | 19.01.2024   | Bajramovic     | Entwicklung der Menü-Logik für die Benutzerführung.             | 120'       |
| 3.A    | 19.01.2024   | Marku  | Implementierung der Funktion zum Hinzufügen von der Website.     | 60'         |
| 4.A    | 19.01.2024   | Marku  | Implementierung der Funktion zum Hinzufügen von Passwörtern.     | 60'         |
| 5.A    | 19.01.2024   | Angelov | Implementierung der Funktion zur Verschlüsselung des Passworts vor der Speicherung, um die Sicherheit der Daten zu erhöhen.       | 120'        |
| 6.A    | 26.01.2024  | Angelov     | Programmierung der Datenbankintegration zum Speichern von Passwörtern. | 120'          |
| 7.A    | 19.01.2024   | Jashari | Implementierung der Anzeige für die Passwortliste.       | 120'           |
| 8.A    | 02.02.2024  | Jashari      | Entwickeln der Logik für das Löschen von Einträgen.             | 120'          |
| 9.A    | 02.02.2024 | Jashari     | Implementierung von Fehlerbehandlungsmechanismen.               | 120'          |
| 10.A    | 23.02.2024 | Bajramovic    | Finalisierung, Verschönerung und Überprüfung aller Funktionen.                 | 120'          |    |
| 11.A    | 23.02.2024 | Alle    | Portfolioeintrag Schreiben.                 | 180'          |




## 3 Entscheiden

Wir haben uns für eine enge Zusammenarbeit im Team entschieden und setzten häufig auf Pair-Programming, um voneinander zu lernen. Dadurch arbeiteten wir eng zusammen und erledigten gemeinsam die geplanten Pakete, selbst wenn diese ursprünglich jemand anderem zugewiesen waren, unterstützten wir einander.

## 4 Realisieren

| AP-№ | Datum | Zuständig | Geplante Zeit | Tatsächliche Zeit |
|------|-------|-----------|---------------|-------------------|
| 1.A | 12.01.2024 | Alle | 240' | 240' |
| 2.A | 19.01.2024  | Bajramovic | 120' | 90' |
| 3.A | 19.01.2024  | Angelov, Marku, Jashari | 60' | 20' |
| 4.A | 26.01.2024 |  Angelov, Marku, Jashari| 60' | 20' |
| 5.A | 02.02.2024 | Angelov, Marku, Jashari | 120' |160' |
| 6.A | 02.02.2024 | Angelov, Marku, Jashari | 120' | 90' |
| 7.A | 02.02.2024 | Jashari, Marku | 120' | 100' |
| 8.A | 23.02.2024 | Jashari, Marku | 120' | 100' |
| 9.A | 23.02.2024 | Jashari | 120' | 60' |
| 10.A | 23.02.2024 | Bajramovic | 120' | 60' |
| 11.A | 23.02.2024 | Alle | 180' | 180' |

## 5 Kontrollieren

### 5.1 Testprotokoll

| TC-№ | Datum      | Resultat | Tester      |
|------|------------|----------|-------------|
| 1.0  | 23.02.2024 | OK       | Team        |
| 2.0  | 23.02.2024 | OK       | Angelov     |
| 3.0  | 23.02.2024 | OK       | Bajramovic  |
| 4.0  | 23.02.2024 | OK       | Marku     |
| 5.0  | 23.02.2024 | OK       | Jashari       |
| 5.1  | 23.02.2024 | OK       | Angelov     |
| 5.2  | 23.02.2024 | OK       | Bajramovic  |
| 6.0  | 23.02.2024 | OK       | Marku     |
| 7.0  | 23.02.2024 | OK       | Jashari       |
| 8.0  | 23.02.2024 | OK       | Angelov     |
| 9.0  | 23.02.2024 | OK       | Bajramovic  |
| 10.0  | 23.02.2024| OK       | Marku     |
