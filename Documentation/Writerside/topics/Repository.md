# Repositories

Ein Repository ist ein **Workspace**, welcher **Dateien trackt und verwaltet**. 

Immer wenn wir Git für ein Projekt, eine App, etc. verwenden wollen, dann müssen wir ein Repository erstellen. Diese sind völlig unabhängig voneinander.

## Repository erstellen

Um ein Repository zu erstellen, nutzen wir das folgende Kommando:

````Bash
git init
````

> Man sollte kein Repository in einem Repository erstellen!

{ style="warning" }

## Status abfragen

Mit dem folgenden Kommando können wir Informationen über unser Git Repository und dessen Inhalt bekommen:

````Bash
git status
````

### Meldungen

Wenn wir kein Git Repository haben, zeigt es folgenden Fehler an:

````Text
fatal: not a git repository
````

Das heisst für uns, dass wir zuerst ein neues Repository mit `git init` erstellen müssen.

Wenn wir aber bereits ein Repository haben, dann zeigt es uns auf welchem Branch wir uns befinden, Commits, die Staging-Area, etc.