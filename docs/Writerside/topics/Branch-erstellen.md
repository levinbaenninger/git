# Verwalten von Branches

## Branches auflisten

Mit dem folgenden Kommando können wir alle unsere Branches im Repository anzeigen:

```Bash
git branch
```

Der Output könnte wie folgt aussehen:

````Bash
* bug/navigation-bar
  chore/remove-dependencies
  feature/teams
  feature/games
  master
````

Dort wo der `*` ist, auf diesem Branch befinden wir uns gerade befinden.

## Branch erstellen

Wir erstellen einen Branch mit dem folgenden Kommando:

````Bash
git branch <branch-name>
````

Das erstellt einen neuen Branch mit dem spezifizierten Namen auf Grundlage des `HEAD`. Dabei wechseln wir noch nicht auf den neuen Branch; der `HEAD` bleibt also gleich.

## Branch wechseln

Um unseren Branch zu wechseln, nutzen wir das folgende Kommando:

````Bash
git switch <branch-name>
````

Mit diesem Kommando verweist der `HEAD` nun auf den Branch. Wenn wir nun hier ein Commit machen existiert dieser nur auf diesem Branch. 

### Schalter

> Mit dem Schalter `-c` erstellen wir gleichzeitig den Branch und wechseln zu ihm:
>
> ````Bash
> git switch -c <branch-name>
> ````

### Regel

> Bevor man zu einem neuen Branch wechselt, sollte man seine Arbeit **immer committen oder stashen**!

{ style="warning" }

## Branch löschen

Mit dem Schalter `-d` können wir einen Branch löschen:

````Bash
git branch -d <branch-name>
````
Bevor wir aber den Branch löschen können, müssen wir auf einen anderen Branch wechseln, bspw `master`.

> Ohne Merge wird Git uns warnen und uns bitten das Kommando mit dem Schalter `-D` erneut aufzurufen:
> 
> ````Bash
> git branch -D <branch-name>
> ````

## Branch umbenennen

Um einen Branch umzubenennen, müssen wir zuerst in den Branch wechseln und dort das folgende Kommando ausführen:

````Bash
git branch -m <new-branch-name>
````

