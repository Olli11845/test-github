# Objects to classes

Objekte werden mit geschweiften Klammern erstellt
Objekte sind gefüllt mit Keys und Values.

Objekte können niemals gleich sein. Nur die Elemente darin.

`Object.keys(objectName)` gibt die einzelnen Parameter eines Objekts aus.
`Object.values(objectName)` gibt alle Values des betrachteten Objekts aus. bspw zum Durchsuchen

`Object.entries(objectName)`  Gibt ein Array aus, welche mehrere Arrays ethält, jeweils dioe Key- Value Pairs

`Object.freeze(objectName)` KANN nicht aufgetaut werden! Es kann danach nciht mehr mutiert werden.

`Object.assign(target,obj1,....)` man kann viele obj. aufnehmen und deren Keys und values in das Target Object packen <br>![obj_assign](https://user-images.githubusercontent.com/104325830/170051366-e58fafdd-6c48-4f10-ae9a-3cd024c8c8ec.JPG)
<br>
wenn der Key schon vorhanden ist wird der Value überschrieben.

damit kann ich auch eine Kopie erstellen. Auch von eingefrorenen Objekten.  object assign gibt referenz zurück <br>![assign](https://user-images.githubusercontent.com/104325830/170052124-0a7b2eca-f163-4e0e-b968-b1f045b10bdd.JPG)
<br>
Wenn ich aber Objekte kopiere die Kopien enthalten funktioniert das nicht. Denn ich kopiere nur die Referenz des Objekts und nciht das Objekt selbst. "Objetke sind einzigartig spielt da mit rein"

**Recap Objects**
<br>![objects_Recap](https://user-images.githubusercontent.com/104325830/170054052-ec4e63e5-e6d3-47e1-9eb5-75db3b3b6d64.JPG)
<br>


## Objekt Methoden und this
In Objekten können Funktionen hinterlegt werden.
quasi Mini Programme in einem großen Programm hinterlegen.

Funktion in einem Objekt --> Methode.<br>![Function in Objetcs](https://user-images.githubusercontent.com/104325830/170059886-96ac3056-5e89-4347-99d6-d3f48e4c4f86.JPG)
<br>
In dem Bild ist es eine anonyme function. Also eine, welche sofort aufgerufen werden kann.

`this` keyword. Bezieht sich immer auf das Object in dem man gerade ist. also `this.x` ruft den x Key des Objektes auf in dem wir gerade stehen <br> 
![this in objects](https://user-images.githubusercontent.com/104325830/170062096-47ce5f58-2959-4c30-b6c0-41410839dd11.JPG) <br>


## this Keyword

**Das this keyword zeigt immer auf seinen execution context**
Achtung: JS kann einen fixen this context setzen

wenn man es im Global scope ausführt zeigt es window an. Oder genauso in Node.js --> es zeigt global object an.







