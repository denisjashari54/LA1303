# Dokumentation LA1303
## Passwort-Manager-Projekt 

Angel Angelov, Erik Marku, Denis Jashari



| Datum      | Version | Zusammenfassung                                                                       |
|------------|---------|---------------------------------------------------------------------------------------|
| [Datum 1]  | 0.0.1   | Projektinitiierung und erste Diskussion über Verschlüsselungsmethoden                 |
| [Datum 2]  | 0.0.2   | Beginn der Programmierung mit Grundfunktionalitäten                                   |
| [Datum 3]  | 0.0.3   | Implementierung der Datenbank zur Speicherung der Passwörter                          |
| [Datum 4]  | 0.0.4   | Implementierung von Verschlüsselungsfunktionen für die sichere Speicherung von Daten  |
| [Datum 5]  | 0.0.5   | Endgültige Tests und Fertigstellung der Dokumentation                                 |

## 1. Informieren

### 1.1 Ihr Projekt

Das Ziel dieses Projekts ist die Entwicklung eines einfachen Passwort-Managers, der es Benutzern ermöglicht, ihre Passwörter sicher zu speichern, anzuzeigen und zu verwalten. Der Passwort-Manager soll eine einfache Konsolenanwendung sein, die die grundlegenden Funktionen eines Passwort-Managers, wie das Hinzufügen, Anzeigen und Löschen von Passwörtern, unterstützt. Zusätzlich wird eine Verschlüsselungsfunktion implementiert, um die Sicherheit der gespeicherten Passwörter zu gewährleisten.


### 1.2 User Stories

| US-Nr. | Verbindlichkeit | Typ         | Beschreibung                                                                                                                                                       |
|--------|-----------------|-------------|-----------------------------------------------------|
| 1      | Muss            | Funktionell | Als Benutzer möchte ich Passwörter zusammen mit der zugehörigen Website und Benutzernamen hinzufügen können, um meine Anmeldedaten sicher zu speichern.    |
| 2      | Muss            | Funktionell | Als Benutzer möchte ich meine gespeicherten Passwörter einsehen können, um Zugriff auf meine Anmeldedaten zu haben.                                               |
| 3      | Muss            | Funktionell | Als Benutzer möchte ich Passwörter aus meinem Speicher löschen können, um veraltete oder nicht mehr benötigte Einträge zu entfernen.                              |
| 4      | Muss            | Funktionell | Als Benutzer möchte ich, dass meine Passwörter verschlüsselt gespeichert werden, um die Sicherheit meiner Daten zu erhöhen.                                   |
| 5      | Muss            | Funktionell | Als Benutzer möchte ich beim Start des Programms die Wahl haben, ein neues Passwort hinzuzufügen oder vorhandene Passwörter anzusehen.                            |
| 6      | Muss            | Funktionell | Als Benutzer möchte ich, dass meine Passwörter sicher in einer Datenbank gespeichert werden, um dauerhaften und sicheren Zugriff zu gewährleisten.            |

### 1.3 Testfälle

| TC-Nr. | Ausgangslage                                 | Eingabe                  | Erwartete Ausgabe                                                                                                         |
|--------|----------------------------------------------|--------------------------|-------------------------------------------------------|
| 1.1    | Programm gestartet, Hauptmenü wird angezeigt | "1"                      | Weiterleitung zum Hinzufügen-Menü; Aufforderung zur Eingabe des Namens der Website, für die das Passwort gespeiche werden soll: "Website: " |
| 1.2    | Website-Namen eingegeben                     | [Website-Name]           | Aufforderung zur Eingabe des Benutzernamens: "Username: " |
| 1.3    | Benutzernamen eingegeben                     | [Benutzername]           | Aufforderung zur Eingabe des Passworts: "Password: "               |
| 1.4    | Passwort eingegeben                          | [Passwort]               | Aufforderung, ob das Passwort verschlüsselt werden soll: "Do you want to encrypt the password? (y/n): "        |
| 1.5    | Verschlüsselungsauswahl getroffen            | "y"                      | Bestätigung, dass das Passwort hinzugefügt (und verschlüsselt) wurde; Rückkehr zum Hauptmenü                   |
| 1.6    | Zurück im Hauptmenü                          | "2"                      | Anzeige aller gespeicherten Passwörter; Frage, ob ein Passwort gelöscht werden soll: "Do you want to delete a password? (y/n): " |
| 1.7    | Zustimmung zum Löschen eines Passworts       | "y"                      | Aufforderung zur Eingabe der ID des zu löschenden Passworts: "Please enter the ID of the password to be deleted: "     |
| 1.8    | Eingabe der ID des zu löschenden Passworts   | [ID]                     | Bestätigung, dass das Passwort gelöscht wurde; Frage, ob ein weiteres Passwort gelöscht werden soll: "Do you want to delete another password? (y/n): " |
| 1.9    | Entscheidung gegen weiteres Löschen          | "n"                      | Rückkehr zum Hauptmenü                                            |
| 1.10   | Im Hauptmenü                                 | "3"                      | Programm wird geschlossen; keine weiteren Aktionen erforderlich                              |
