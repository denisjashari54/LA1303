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

### 1.4 Diagramme
![Hauptprogramm 1](https://github.com/denisjashari54/LA1303/assets/112430127/82f61273-bd01-439a-9718-be3ffa20d551)

## 2 Planen

| AP-Nr. | Frist      | Zuständig   | Beschreibung                                                    | Geplante Zeit |
|--------|------------|-------------|-----------------------------------------------------------------|---------------|
| 1.A    | [Datum 1]  | Alle        | Informationssammlung und -austausch über Projektziele.          | 4 Std         |
| 2.A    | [Datum 2]  | Bajramovic     | Entwicklung der Menü-Logik für die Benutzerführung.             | 2 Std         |
| 3.A    | [Datum 3]  | Marku  | Implementierung der Funktion zum Hinzufügen von Passwörtern.     | 2 Std         |
| 4.A    | [Datum 4]  | Jashari | Implementierung der Anzeige für die Passwort Liste.       | 2 Std         |
| 5.A    | [Datum 5]  | Angelov     | Programmierung der Datenbankintegration zum Speichern von Passwörtern. | 2 Std         |
| 6.A    | [Datum 6]  | Marku  | Implementierung der Verschlüsselungsfunktionen für mehr Sicherheit. | 2 Std         |
| 7.A    | [Datum 7]  | Angelov      | Entwickeln der Logik für das Löschen von Einträgen.             | 2 Std         |
| 8.A    | [Datum 8]  | Jashari     | Implementierung von Fehlerbehandlungsmechanismen.               | 2 Std         |
| 9.A    | [Datum 9]  | Bajramovic    | Finalisierung und Überprüfung aller Funktionen.                 | 2 Std         |

## 3 Entscheiden


Wir haben in der Gruppe die Arbeitspakete fair verteilt, sodass wir alle zum Implementieren beitragen. Dadurch haben wir auch eine gute Zeiteinteilung erreicht.

## 4 Realisieren

| AP-№ | Datum | Zuständig | Geplante Zeit | Tatsächliche Zeit |
|------|-------|-----------|---------------|-------------------|
| 1.A | [Datum 1] | Alle | 240' | 240' |
| 2.A | [Datum 2] | Bajramovic | 120' | 90' |
| 3.A | [Datum 3] | Marku | 120' | 60' |
| 4.A | [Datum 4] | Jashari | 120' | 80' |
| 5.A | [Datum 5] | Angelov | 120' | 90' |
| 6.A | [Datum 6] | Marku | 120' | 90' |
| 7.A | [Datum 7] | Angelov | 120' | 90' |
| 8.A | [Datum 8] | Jashari | 120' | 80' |
| 9.A | [Datum 9] | Bajramovic | 120' | 70' |

## 5 Kontrollieren

### 5.1 Testprotokoll

| TC-№ | Datum      | Resultat | Tester      |
|------|------------|----------|-------------|
| TC-1 | 23.02.2024 | OK       | Bajramovic  |
| TC-2 | 23.02.2024 | OK       | Angelov     |
| TC-3 | 23.02.2024 | OK       | Marku       |
| TC-4 | 23.02.2024 | OK       | Jashari     |
| TC-5 | 23.02.2024 | OK       | Bajramovic  |
| TC-6 | 23.02.2024 | OK       | Angelov     |
| TC-7 | 23.02.2024 | OK       | Marku       |
| TC-8 | 23.02.2024 | OK       | Jashari     |
| TC-9 | 23.02.2024 | OK       | Bajramovic  |
