# Fast-Forward Merge

Mit dem folgenden Kommando mergen wir einen Branch:

````Bash
git merge <branch-name>
````

### Beispiel

Wenn wir also bspw. in den `master` Branch den Branch `bugfix` mergen wollen, machen wir Folgendes:

````Bash
git switch master
git merge bugfix
````

![merge.png](merge.png) { width="550" thumbnail="true" }

Diese Art von Merge heisst **Fast-Forward**, da der `master` Branch lediglich die Commits vom `bugfix` Branch nachholt. Dabei darf `master` keine neuen Commits haben. 

> Bei Fast-Forward Merges können keine Konflikte entstehen!