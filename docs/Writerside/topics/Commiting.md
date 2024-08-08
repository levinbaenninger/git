# Commiting

Commiting ist das wahrscheinlich wichtigste Feature in Git. Ein Commit ist ein Snapshot unseres Repositories. Es speichert alle Änderungen, Neuerungen, etc. sodass wir in einem späteren Zeitpunkt darauf zugreifen können.

Jeder dieser Snapshots hat eine kleine Beschreibung, was genau geändert wurde. Um ein Commit aber auszuführen, müssen wir die Dateien, die wir zu einem Commit hinzufügen wollen, in die Staging-Area bringen.

## Git Add

Mit `git status` können wir überprüfen welche Änderungen gemacht wurden im Vergleich zum letzten Commit und mit dem folgenden Commando können wir diese Files in die Staging-Area bringen:

````Bash
git add <file> <file> ... <file>
````

Um Dateien wieder aus der Staging-Area zu entfernen, nutzen wir folgendes Kommando: 

````Bash
git rm --cached <file> <file> ... <file>
````

## Git Commit

Nun können wir die Dateien, die wir in die Staging-Area hinzugefügt haben zu einem Commit zusammenfassen:

````Bash
git commit -m "<commit-message>"
````

## Git Log

Um alle unsere Commits anzuschauen, nutzen wir folgendes Kommando:

````Bash
git log
````

Hier sehen wir alle Commits, die gemacht wurden. Wir sehen den Hashcode, die Nachricht, das Commit-Datum und den Autor.