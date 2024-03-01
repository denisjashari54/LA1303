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
| 3      | Muss            | Funktional  | Als Benutzer möchte ich die ID eingeben können, um zu wissen, welches Konto betroffen ist.  |
| 4      | Muss            | Funktional  | Als Benutzer möchte ich das Passwort eingeben können, damit es zusammen mit der Website und dem Benutzernamen gespeichert wird. |
| 5      | Muss            | Funktional  | Als Benutzer möchte ich die Möglichkeit haben, mein Passwort vor der Speicherung zu verschlüsseln, um die Sicherheit meiner Daten zu erhöhen. |
| 6      | Muss            | Funktional  | Als Benutzer möchte ich eine Liste aller gespeicherten Passwörter einsehen können, um einen Überblick zu erhalten.  |
| 7      | Muss            | Funktional  | Als Benutzer möchte ich die Möglichkeit haben, ein gespeichertes Passwort zu löschen, um meine Daten aktuell zu halten. |
| 8      | Kann            | Funktional  | Als Benutzer möchte ich, dass das Programm Fehlermeldungen angemessen behandelt, um die Benutzererfahrung zu verbessern.  |
| 9     | Muss            | Funktional  | Als Benutzer möchte ich, dass meine Daten nach dem Beenden des Programms gespeichert bleiben und bei erneutem Start verfügbar sind. |
| 10     | Kann            | Funktional  | Als Benutzer erwarte ich eine benutzerfreundliche Oberfläche, die die Nutzung des Programms intuitiv und einfach macht. |



### 1.3 Testfälle

| TC-Nr. | Ausgangslage                                 | Eingabe                  | Erwartete Ausgabe                                                                                                         |
|--------|----------------------------------------------|--------------------------|-------------------------------------------------------|
| 1.0   | Programm gestartet, Hauptmenü wird angezeigt | "1"                      | Weiterleitung zum Hinzufügen-Menü; Aufforderung zur Eingabe des Namens der Website, für die das Passwort gespeichert werden soll: "Website: " |
| 2.0    | Website-Namen eingegeben                     | [Website-Name]           | Aufforderung zur Eingabe des Benutzernamens: "Username: " |
| 3.0    | Benutzernamen eingegeben                     | [Benutzername]           | Aufforderung zur Eingabe des Passworts: "Password: "               |
| 4.0    | Passwort eingegeben                          | [Passwort]               | Aufforderung, ob das Passwort verschlüsselt werden soll: "Do you want to encrypt the password? (y/n): "        |
| 5.0    | Verschlüsselungsauswahl getroffen            | "y"                      | Bestätigung, dass das Passwort hinzugefügt (und verschlüsselt) wurde; Rückkehr zum Hauptmenü                   |
| 6.0    | Zurück im Hauptmenü                          | "2"                      | Anzeige aller gespeicherten Passwörter; Frage, ob ein Passwort gelöscht werden soll: "Do you want to delete a password? (y/n): " |
| 7.0    | Zustimmung zum Löschen eines Passworts       | "y"                      | Aufforderung zur Eingabe der ID des zu löschenden Passworts: "Please enter the ID of the password to be deleted: "     |
| 7.1    | Eingabe der ID des zu löschenden Passworts   | [ID]                     | Bestätigung, dass das Passwort gelöscht wurde; Frage, ob ein weiteres Passwort gelöscht werden soll: "Do you want to delete another password? (y/n): " |
| 7.2    | Entscheidung gegen weiteres Löschen          | "n"                      | Rückkehr zum Hauptmenü; Daten                                           |
| 8.0 | Im Hauptmenü | "4" |Es erscheint eine rote Fehlermeldung, und man kann daraufhin eine weitere Eingabe machen. |
| 9.0 | Im Hauptmenü | "3" | Das Programm wird beendet und Daten werden gespeichert. |
| 10.0 | Programm wieder starten; im Hauptmenü | "2" | Vorherige gespeicherte Daten werden hervorgehoben. |



### 1.4 Diagramme
![Hauptprogramm 1](https://github.com/denisjashari54/LA1303/assets/112430127/82f61273-bd01-439a-9718-be3ffa20d551)

## 2 Planen

| AP-Nr. | Frist      | Zuständig   | Beschreibung                                                    | Geplante Zeit |
|--------|------------|-------------|-----------------------------------------------------------------|---------------|
| 1.A    | 12.01.2024 | Alle        | Informationssammlung und -austausch über Projektziele.          | 240'|
| 2.A    | 19.01.2024   | Bajramovic     | Entwicklung der Menü-Logik für die Benutzerführung.             | 120'       |
| 3.A    | 19.01.2024   | Marku  | Implementierung der Funktion zum Hinzufügen von der Website.     | 60'         |
| 4.A    | 19.01.2024   | Marku  | Implementierung der Funktion zum Hinzufügen von dem Benutzernamen.     | 60'         |
| 5.A    | 19.01.2024   | Marku  | Implementierung der Funktion zum Hinzufügen von Passwörtern.     | 60'         |
| 6.A    | 19.01.2024   | Angelov, Marku | Implementierung der Funktion zur Verschlüsselung des Passworts vor der Speicherung, um die Sicherheit der Daten zu erhöhen.       | 120'        |
| 7.A    | 26.01.2024  | Angelov     | Programmierung der Datenbankintegration zum Speichern von Passwörtern. | 120'          |
| 8.A    | 19.01.2024   | Jashari | Implementierung der Anzeige für die Passwortliste.       | 120'           |
| 9.A    | 02.02.2024  | Angelov      | Entwickeln der Logik für das Löschen von Einträgen.             | 120'          |
| 10.A    | 02.02.2024 | Jashari     | Implementierung von Fehlerbehandlungsmechanismen.               | 120'          |
| 11.A    | 23.02.2024 | Bajramovic    | Finalisierung, Verschönerung und Überprüfung aller Funktionen.                 | 120'          |    |
| 12.A    | 23.02.2024 | Alle    | Portfolioeintrag Schreiben.                 | 180'          |




## 3 Entscheiden

Wir haben uns entschieden, eng in der Gruppe zusammenzuarbeiten und viel Pairprogramming zu machen, um voneinander zu profitieren.

## 4 Realisieren

| AP-№ | Datum | Zuständig | Geplante Zeit | Tatsächliche Zeit |
|------|-------|-----------|---------------|-------------------|
| 1.A | 12.01.2024 | Alle | 240' | 240' |
| 2.A | 19.01.2024  | Bajramovic | 120' | 90' |
| 3.A | 19.01.2024  | Marku | 60' | 80' |
| 4.A | 19.01.2024  | Marku | 60' | 10' |
| 5.A | 26.01.2024 | Marku| 60' | 10' |
| 6.A | 02.02.2024 | Angelov, Marku | 120' |180' |
| 7.A | 02.02.2024 | Angelov | 120' | 90' |
| 8.A | 02.02.2024 | Jashari | 120' | 120' |
| 9.A | 23.02.2024 | Angelov | 120' | 140' |
| 10.A | 23.02.2024 | Jashari | 120' | 80' |
| 11.A | 23.02.2024 | Bajramovic | 120' | 90' |
| 12.A | 23.02.2024 | Alle | 180' | 150' |

## 5 Kontrollieren

### 5.1 Testprotokoll

| TC-№ | Datum      | Resultat | Tester      |
|------|------------|----------|-------------|
| 1.0  | 23.02.2024 | OK       | Team        |
| 2.1  | 23.02.2024 | OK       | Angelov     |
| 2.2  | 23.02.2024 | OK       | Marku       |
| 2.3  | 23.02.2024 | OK       | Jashari     |
| 3.0  | 23.02.2024 | OK       | Bajramovic  |
| 4.0  | 23.02.2024 | OK       | Angelov     |
| 5.0  | 23.02.2024 | OK       | Marku       |
| 5.1  | 23.02.2024 | OK       | Jashari     |
| 5.2  | 23.02.2024 | OK       | Bajramovic  |
| 6.0  | 23.02.2024 | OK       | Angelov     |
| 7.0  | 23.02.2024 | OK       | Marku       |
| 8.0  | 23.02.2024 | OK       | Jashari     |
| 9.0  | 23.02.2024 | OK       | Bajramovic  |
| 10.0  | 23.02.2024| OK       | Angelov     |
