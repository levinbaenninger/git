# Main/Master Branch

Der `main` bzw. `master` Branch ist der Standardbranch unseres Repositories, das heisst, dass wir immer auf einem Branch arbeiten. 

> Er hat keine anderen oder weiteren Features, als alle anderen Branches.

In den meisten Projekten ist das der Branch, worauf alle Änderungen zusammenlaufen, die für die Produktion bestimmt sind. Es ist üblich, dass dieser Branch stabil gehalten wird und alle neuen Features und Änderungen in separaten Branches entwickelt werden. Sobald diese Änderungen getestet und überprüft wurden, werden sie in den Main bzw. Master Branch [**gemerged**](Merging.md).

![main-branch.png](main-branch.png) { width="550" thumbnail="true" }

Oben sehen wir, wie ein neues Feature wieder in den `master` Branch eingeführt wird.

## Main oder Master?

In 2020 hat sich GitHub dazu entschieden, den `master` Branch in `main` umzubenennen. Jedoch benutzt Git selbst immer noch `master` für den Standardbranch.