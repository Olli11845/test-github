# testing
manual testing
and automated testing

### manual testing
manuelles testen ist das was man automatisch schon nebenbei macht. Problem: Es ist nicht skalierbar.

reicht auf keinen Fall aus

### automated testing
muss vom Tooling getrennt sein.

von google
small tests
medium tests
large tests

--> es geht um die Sicherheit und Abhängigkeit der Tests

bei uns:
Unit Test --> Tests der keinen Einfluss auf den DOM hat.

End-to-End Testet die ganze Application im Browser



### pure functions

gleiche Parameter rein dann gibt sie immer das gleiche aus.
darf z.b. nicht lesen oder schreiben in globale Variablen


wenn globale Variablen gebraucht werden, kann man diese nochmal selbst übergeben.

### End to End
End to End tut so als wäre der Test ein User.
langsamer als Unit Test


### Test Pyramide

wenig manuelle Tests
mittel E2E
viele unit tests


wichtig. Keyword `cy` bei den cyprus Befehlen
Die API ist fluent... also alles in einer Reihe

`cy.get("selector")`

`cy.should("selector")`

`beforeEach` Funktion. Zum Beispiel: Vor jedem Test öffnest du diese Seite.


Querying Elements
cy.get(); so wie querySelectorAll.
cy.get("article").find("h2")


Eigene Attribute anlegen
`data-cy`="todo-input"

`click`
`blur`
`check`
`type`

man kann alles machen was man auch als regulärer Besucher machen kann.

check nochmal:

`cypress docs`

### Refactoring

Unit Testing in der Regel in Node environment. D.h. query Selector oder addEventlistener funktionieren nicht

ecma script ist nachträglich hinzugekommen.

daher muss `type:"module"` hinzufügen





