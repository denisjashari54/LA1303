# Dokumentation LA1303
## Passwort-Manager-Projekt 

Angel Angelov, Erik Marku, Denis Jashari



| Datum      | Version | Zusammenfassung                                                                       |
|------------|---------|---------------------------------------------------------------------------------------|
| 12.01.2024 | 0.0.1   | Projektinitiierung und erste Diskussion über Verschlüsselungsmethoden                 |
| 19.01.2024  | 0.0.2   | Beginn der Programmierung mit Grundfunktionalitäten                                   |
| 26.01.2024  | 0.0.3   | Implementierung der Datenbank zur Speicherung der Passwörter                          |
| 02.02.2024  | 0.0.4   | Implementierung von Verschlüsselungsfunktionen für die sichere Speicherung von Daten  |
| 23.02.2024  | 0.0.5   | Protokol schreiben                       |

## 1. Informieren

### 1.1 Ihr Projekt

Das Ziel dieses Projekts ist die Entwicklung eines einfachen Passwort-Managers, der es Benutzern ermöglicht, ihre Passwörter sicher zu speichern, anzuzeigen und zu verwalten. Der Passwort-Manager soll eine einfache Konsolenanwendung sein, die die grundlegenden Funktionen eines Passwort-Managers, wie das Hinzufügen, Anzeigen und Löschen von Passwörtern, unterstützt. Zusätzlich wird eine Verschlüsselungsfunktion implementiert, um die Sicherheit der gespeicherten Passwörter zu gewährleisten.


### 1.2 User Stories

| US-Nr. | Verbindlichkeit | Typ         | Beschreibung                                                                                          |
|--------|-----------------|-------------|-------------------------------------------------------------------------------------------------------|
| 1      | Muss            | Funktional  | Als Benutzer möchte ich beim Start des Programms wählen können, ob ich Passwörter ansehen oder hinzufügen möchte. |
| 2      | Muss            | Funktional  | Als Benutzer möchte ich ein Passwort zusammen mit relevanten Informationen (Website, Benutzername) hinzufügen können.  |
| 2.1      | Muss            | Funktional  | Als Benutzer möchte ich den Namen der Website angeben können, um zu wissen, zu welcher Anwendung das Passwort gehört.  |
| 2.2      | Muss            | Funktional  | Als Benutzer möchte ich den Benutzernamen eingeben können, um zu wissen, welches Konto betroffen ist.  |
| 2.3      | Muss            | Funktional  | Als Benutzer möchte ich das Passwort eingeben können, damit es zusammen mit der Website und dem Benutzernamen gespeichert wird. |
| 3      | Muss            | Funktional  | Als Benutzer möchte ich die Möglichkeit haben, mein Passwort vor der Speicherung zu verschlüsseln, um die Sicherheit meiner Daten zu erhöhen. |
| 4      | Muss            | Funktional  | Als Benutzer möchte ich eine Liste aller gespeicherten Passwörter einsehen können, um einen Überblick zu erhalten.  |
| 5      | Muss            | Funktional  | Als Benutzer möchte ich die Möglichkeit haben, ein gespeichertes Passwort zu löschen, um meine Daten aktuell zu halten. |
| 6    | Kann            | Funktional  | Als Benutzer möchte ich, dass das Programm Fehlermeldungen angemessen behandelt, um die Benutzererfahrung zu verbessern.  |
| 7     | Muss            | Funktional  | Als Benutzer möchte ich, dass meine Daten nach dem Beenden des Programms gespeichert bleiben und bei erneutem Start verfügbar sind. |
| 8    | Muss            | Funktional  | Als Benutzer möchte ich, dass alle eingetragenen Daten sicher in einer Datenbank gespeichert werden. |

| 9     | Kann            | Funktional | Als Benutzer erwarte ich eine benutzerfreundliche Oberfläche, die die Nutzung des Programms intuitiv und einfach macht. |

### 1.3 Testfälle

| TC-Nr. | Ausgangslage                                 | Eingabe                  | Erwartete Ausgabe                                                                                                         |
|--------|----------------------------------------------|--------------------------|-------------------------------------------------------|
| 1.0   | Programm gestartet, Hauptmenü wird angezeigt | "1"                      | Weiterleitung zum Hinzufügen-Menü; Aufforderung zur Eingabe des Namens der Website, für die das Passwort gespeiche werden soll: "Website: " |
| 2.1    | Website-Namen eingegeben                     | [Website-Name]           | Aufforderung zur Eingabe des Benutzernamens: "Username: " |
| 2.2    | Benutzernamen eingegeben                     | [Benutzername]           | Aufforderung zur Eingabe des Passworts: "Password: "               |
| 2.3    | Passwort eingegeben                          | [Passwort]               | Aufforderung, ob das Passwort verschlüsselt werden soll: "Do you want to encrypt the password? (y/n): "        |
| 3.0    | Verschlüsselungsauswahl getroffen            | "y"                      | Bestätigung, dass das Passwort hinzugefügt (und verschlüsselt) wurde; Rückkehr zum Hauptmenü                   |
| 4.0    | Zurück im Hauptmenü                          | "2"                      | Anzeige aller gespeicherten Passwörter; Frage, ob ein Passwort gelöscht werden soll: "Do you want to delete a password? (y/n): " |
| 5.0    | Zustimmung zum Löschen eines Passworts       | "y"                      | Aufforderung zur Eingabe der ID des zu löschenden Passworts: "Please enter the ID of the password to be deleted: "     |
| 5.1    | Eingabe der ID des zu löschenden Passworts   | [ID]                     | Bestätigung, dass das Passwort gelöscht wurde; Frage, ob ein weiteres Passwort gelöscht werden soll: "Do you want to delete another password? (y/n): " |
| 5.2    | Entscheidung gegen weiteres Löschen          | "n"                      | Rückkehr zum Hauptmenü; Daten                                             |
| 6.0 | Im Hauptmenü | "4" | Passiert nicht und wartet auf weitere Eingabe. Das Programm reagiert nicht auf eine nicht richtige Eingabe und bleibt im Hauptmenü. |
| 7.0 | Im Hauptmenü | "3" | Das Programm wird beendet und Daten werden gespeichert. |
| 8.0 | Programm wieder starten; Im Hauptmenü | "2" | Vorherige gespeicherte Daten werden hervorgehoben. |


### 1.4 Diagramme
![Hauptprogramm 1](https://github.com/denisjashari54/LA1303/assets/112430127/82f61273-bd01-439a-9718-be3ffa20d551)

## 2 Planen

| AP-Nr. | Frist      | Zuständig   | Beschreibung                                                    | Geplante Zeit |
|--------|------------|-------------|-----------------------------------------------------------------|---------------|
| 1.A    | 12.01.2024 | Alle        | Informationssammlung und -austausch über Projektziele.          | 4 Std         |
| 2.A    | 19.01.2024   | Bajramovic     | Entwicklung der Menü-Logik für die Benutzerführung.             | 2 Std         |
| 3.A    | 19.01.2024   | Marku  | Implementierung der Funktion zum Hinzufügen von Passwörtern.     | 2 Std         |
| 4.A    | 19.01.2024   | Jashari | Implementierung der Anzeige für die Passwort Liste.       | 2 Std         |
| 5.A    | 26.01.2024  | Angelov     | Programmierung der Datenbankintegration zum Speichern von Passwörtern. | 2 Std         |
| 6.A    | 02.02.2024 | Marku  | Implementierung der Verschlüsselungsfunktionen für mehr Sicherheit. | 2 Std         |
| 7.A    | 02.02.2024  | Angelov      | Entwickeln der Logik für das Löschen von Einträgen.             | 2 Std         |
| 8.A    | 02.02.2024 | Jashari     | Implementierung von Fehlerbehandlungsmechanismen.               | 2 Std         |
| 9.A    | 23.02.2024 | Bajramovic    | Finalisierung und Überprüfung aller Funktionen.                 | 2 Std         |

## 3 Entscheiden


Wir haben in der Gruppe die Arbeitspakete fair verteilt, sodass wir alle zum Implementieren beitragen. Dadurch haben wir auch eine gute Zeiteinteilung erreicht.

## 4 Realisieren

| AP-№ | Datum | Zuständig | Geplante Zeit | Tatsächliche Zeit |
|------|-------|-----------|---------------|-------------------|
| 1.A | 12.01.2024 | Alle | 240' | 240' |
| 2.A | 19.01.2024  | Bajramovic | 120' | 90' |
| 3.A | 19.01.2024  | Marku | 120' | 60' |
| 4.A | 19.01.2024  | Jashari | 120' | 80' |
| 5.A | 26.01.2024 | Angelov | 120' | 90' |
| 6.A | 02.02.2024 | Marku | 120' | 90' |
| 7.A | 02.02.2024 | Angelov | 120' | 90' |
| 8.A | 02.02.2024 | Jashari | 120' | 80' |
| 9.A | 23.02.2024 | Bajramovic | 120' | 70' |

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
| 6.0  | 23.02.2024 | OK       | Bajramovic  |
| 7.0  | 23.02.2024 | OK       | Bajramovic  |
| 8.0  | 23.02.2024 | OK       | Bajramovic  |
