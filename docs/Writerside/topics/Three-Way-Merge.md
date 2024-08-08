# Three-Way-Merge

Ein Three-Way-Merge entsteht, wenn keine Fast-Forward Merge möglich ist. Das heisst, dass auf dem Branch in den wir mergen wollen seit der Erstellung des Branches Änderungen vorgenommen wurden.

Diese Merges können deutlich schwieriger zu lösen sein, da Konflikte entstehen können. Die Syntax funktioniert in erster Linie genau gleich:

````Bash
git merge <branch-name>
````

Wenn keine Konflikte entstehen, dann erstellt uns Git einen neuen Commit mit den Daten der zusammengeführten Branches.

![three-way-merger.png](three-way-merger.png) { width="550" thumbnail="true" }

## Konflikte

Bei diesem Prozess können jedoch Konflikte entstehen, wenn z.B. auf einem Branch Zeile 49 gelöscht wird und auf dem anderen Zeile 49 bearbeitet wird. Hier weiss Git nicht was es machen soll und frägt uns als Entwickler, welche Änderungen Git übernehmen soll.

Wir werden solch eine Fehlermeldung bekommen, falls dieser Fall auftritt:

````Bash
CONFLICT (content): Merge conflict README.md
Automatic merge failed; fix conflicts and then commit the result.
````

Unsere Datei mit Konflikten sieht ein wenig anders aus:

````Text
Here is some content not affected by the conflict
<<<<<<< HEAD
This is conflicted text from HEAD
=======
This is conflicted text from feature branch
>>>>>>> feature;
````

Hier können wir nun als Entwickler entscheiden, was behalten werden sollte, indem wir diese Zeichen, also `<`, `=` und `>`, wieder entfernen.

Wir können einerseits das vom `HEAD` annehmen, das vom `feature` Branch oder beides:

````Text
Here is some content not affected by the conflict
This is conflicted text from feature branch
````

Hier entscheiden wir uns dafür, dass wir das vom `feature` Branch behalten wollen. Dieses File committen wir nun, um mit dem Mergen fortfahren.