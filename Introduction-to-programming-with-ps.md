# Introduction to programming

p5 ist eine libary und bietet Möglichkeiten Grafiken in Javascript darzustellen

Alle Funktionen in p5: editor.p5js.org
> man sollte Account erstellen

function > sind gebündelte Einzelschritte.

2 Funktionen
`setup` = Wird am Anfang einmal ausgeführt
`draw` = wird immer fortlaufend aufgerufen. Beim Browser ca alle 16ms

Auto-refresh-option. Wenn das eingestellt ist muss man nicht bei jeder Änderung auf play drücken.


## Initial bulding blocks

program --> ist eine Sammlung von Anweisungen

function sind einzelschritte der Programme. Sprache kann von der Sprache oder der Bibliothek definiert sein.
function ist eine definition davon was passieren wird.

es muss eine Setup und evtl draw function geben. So wird die function aufgerufen

eine function muss definiert werden --> und abgerufen werden

wichtig aufbau fuction definieren

function functionname () {
code ;
code ;
}

functionen sind auch in der libary vorhanden
function (setup)
function circle()

Name von Funktionen in folgender Schreibweise. "calculateThis" camel case

eine function kann Paramenter haben,

function functionName (parameter1, parameter2) {
}

achtung function draw greift immer wieder ein. Auf Überschreiben achten


Kommentrae in JS
`//`

oder multiline comments
/*
*/

console.log("This is a setup function");


### drwaing

background(0,0,255);
es gibt x und y achse
farben von 0 blak bis 255 white
255,0,0 --> RGB
Namen wie in css geht auch

circle (200,200,100) bei 200/200 100 groß

rect also REchteck function
rect(x koordinate, y koordinate, x Länge, y Länge)


stroke() und fill()
stroke definiert die outline color stroke(color);
fill(color);

noStroke(); geht auch

strokeWeight(); wie dick ist der Rand


### mouse interaction and randomness
mouseX und mouseY sind variablen und geben so die Position der Maus an
draw kann erzeugt werden, wenn background function ausgelassen wird.

random(10); Einen wert zwischen 0 und 10
Random(5.01,6.10)


## Variables

let variableName = VariableWert

let  muss einmal definiert werden und kann sich danach verändern

alt: `var` in GEdanken zu let ändern.

Schreibart: camelCase. Name darf nicht kollidieren mit Keywords

auf Reihenfolge der Deklaration achten!


##Scopes

Sichtbarkeit der Variable hängt davon ab wo sie deklariert wurde. Beispiel: Innerhalb einer function nur nach unten weiter

Variablen die in einem Block definiert sind, sind nur in diesem Block sichtbar. Eine Definition geht auch nciht aus dem Block raus.
Bei VAR ist es anders. Da gehen werte aus der function raus

Außerhalb von Funktionen: Global Scope

Refactoring: Wir ändern den Code ab. ZB auf eine neue Version



### Data Types, Expressions und Operators

undefined heißt sie ist deklariert aber noch kein Wert bekannt
Number
String
Boolean

Special values undefined und null

in die selbe Variable niemals verschiedene Datentypen reinschreiben

>
<
>=
<=
==
===

Immer den strict equal operator benutzen `===`

AND &&
OR ||

logical not !
dreht true in false und umgekehrt


Implicit ist coercions ist der GRund warum andere JavaScript hassen
1 kann als true gesehen werden
0 kann als false gesehen werden
Bei beiden wenn man mit == arbeitet

### functions

funktionen führe eine Aktion aus
Funktionen können Parameter haben
Funktionen können putput Values haben

in () kommen die Values, welche in die Funktion wollen


**um einen Output zu bekommen...**
`return`
in die function schreiben. Was vor function steht wird ausgegeben


`text`
`keyIsPressed`
`key`
" Bsp: key === "1" "


Diese beiden kombiniert kann zum umstellen von Farben genutzt werden

**Wichtig. Switch Cases**
Können große if-else Bäume ersetzen
switch('Bedingung'):
...
break;
switch('')...

default:  <--- Das ist der Standard

**Fade out effect**
Es wird über ein statisches Bild immer wieder ein neuesLayer drübergelegt. Wenn man das ganz an die Mausposition setzt und dynmaisch macht bekommt man eine Spur

Kurzschreibweise 
+= für a=a+1

**Javascript Objekte** Objekt ist ein Datenspeicher

**Wichtig**
let person {name: "Peter" , age: 99}

let comet {
x=0,
y=0}

Key names in lower Case schreiben
Keys löschen
`delete`

delete Pos.x;
löscht den key innerhalb des Objekts


Increment und Decrement
varName++ oder varName--


### Value and Reference
es gibt primitive und strukturelle Datentypen

diese werden abgerufen über call by value und call by reference


primitive datentypen: number, string, boolean
structural Types: Array, Object

call by value
a=0
b=a
a=1
console.log ==> b bleibt 0


call by reference
variable hält nur eine Referenz auf das Objekt. Änderungen des Objektes gehen mit
