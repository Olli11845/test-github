# Web App Basics

Alle Webseiten haben im Prinzip die gleichen Funktionen

Read input
Change HTML elements
create new html elements
do somethin when somethin happens
load data

Alles erkennt man in der ToDo App.

## Add JS to HTML

`script` um Funktionalität zu laden. logic und code gelanden in HTML
script wird in HTML (Head, oder Body) eingefügt. dazwischen kommt dann der JS Code
wenn kein Type angegeben wird ist es standardmäßig Javascript

grundsätzlich ist jeder JS Code sichtbar. Man kann diese Sichtbarkeit über ES modules einschränken

man kann auch auf deklarationen aus vorigen Skriptteilen zugreifen

Ich kann javascript Dateien auch laden. `.js`kennzeichnet Javascript Dateien --> In HTML ruft man das mit <script src="script.js"></script> wenn beide Dateien im gleichen Ordner sind

Javascript Dateien oder scripts werden in ihrer geschriebenen Reihenfolge ausgeführt

JS Dateien immer am Ende des HTML Dokuments --> Damit zunächst das HTML Zeug geladen wird.

Js dateien innerhalb des Dokuments können `defer`oder àsync`Attribute enthalten. Die könnte den Standard ändern. <-- Ladereihenfolge wird geändert


## Browser Environment

console.log() schreibt in die Konsole des Browsers
console.warn() schreibt auf die debbugging Konsole


`window` verweist auf das Tab, welches in diesem Browser läuft. `windows.console.log()`
`document` auch global verfügbar. document.title ist der Titel des Dokuments, `document.head`, `document.body`

Also kann ich im JS etwas ändern

document.title = "Hello"


## The Document Object Model aka DOM

DOM = Ist die Api die mit dem HTML dokument interagiert

A **node** kann folgendes sein: Ein HTML Element, ein Kommenatr, ein Stück eines HTML Elements

nodes können genutzt werden um Elemente gleicher Klasse zu bearbeiten.

Jede Node hat eine Klasse --> Es können auch mehr sein.

check mdn web docs --> element.


children property --> mit der Children property kann ich mir die Liste aller Kinderelemente geben lassen.

bsp: document.body.children;

`childnodes`sind alle (nicht nur Elemente, sondern auch Zeichen Steuerzeichen etc.)
bsp.: document.body.childnodes


queryselector ==> innerhalb eines Elements nach Elementen suchen.
body
.cool
main > section
main header --> im main nach Header suchen.

gibt **das erste Element** zurück was darauf passt.
Wenn ich nichts finde --> "null"



### find multiple elements with qerySelectorAll method

document.querySelectorAll("article")
ich bekomme alle article die im Document sind.


## Events and Event Handling

bsp etwas wird geklickt.

es gibt 3 Event Phasen. von oben zu dem Elemt wo es passiert (capture Phase, es trifft ein (Target Phase) und es wieder zur Wurzel (Bubble Phase)

Event Types and namnes
click
keyup,keydown,keypress
input, change

Event reference on MDN

`addEventListener(eventType, callback)`

wenn ich darüber liegende Buttons habe werden auch diese ausgeführt (bubble Phase). --> der addEventListener nutzt die bubble Phase.

### nur Target Phase nutzen
Wenn ich nur die Target Phase nutzen will `addEventListener(eventType, callback, true)`  <--- braucht man selten


ich kann auch in die Callback funktion den Parameter mitgeben. Also mit hereingeben ob ich z.B. über einen Klick dorthin gelangt bin.
function(event)
event.target --> auf welchen Button wurde geklickt
event.eventPhase --> in welcher Phase wurde es gewählt (0 = event is not processed, 1= Capture Phase, 2 Target Phase, 3 bubble Phase)
event.currentTarget --> auf welchem Element befinden wir uns gerade (als auch das wo wir nur drüber wandern.

event.stopPropagation --> es wird an diesem Punkt abgebrochen und wandert nicht weiter durch die Phasen (Capture, Target, Bubble)
use cases: wenn ich eine Liste mit gleichen Dingen habe. 



this verweist darauf wo die funktion ausgelöst wurde. Bspw.: console.log(this()) --> eventButton

Beispiele aus dem Lice Coding
<br>
![buttonclick](https://user-images.githubusercontent.com/104325830/171432101-9ea76daf-e20b-4510-985b-fbb32b9072bb.JPG)
<br>


## Styles ändern

`element.style` wir greifen auf Styling Objekt zu
`element.classList`  List of CSS classes of the element
`element.className` eher schlecht zu bennutzen


style --> alle befehle werden im Camel Case geschrieben

class List kann auch Befehle ausführen --> add, remove, toggle



## Element Attribute
Attribute List MDN Attribute

`disabled`
`src`
`hidden`
`value`


`hasAttribute()`
`setAttribute(name, value)` <--> setzt neu oder aktualisiert

oder
booleanAtrributes
diese brauchen keinen Wert btn.setAttribute("disabled","");

`removeAttribute(attributeName)`

`getAttribute` --> zeigt die Attribute an


`element.type`
`element.value`


custom attributes sind auch mögliche. Diese Strings müssen mit data-*

Beispiel:
input.setAttribbute("disabled","")




### the text content of elements

`textContent` gibt den Text des Elements und aller Kinder Elemente inklusive aller script und style tags

`innerText` gibt den Text vom Elementen und von den Kinderelementen. wenn visibility auf hidden gesetzt ist wird es angezeigt. Wenn es auf display:none gesetzt ist dann nicht


`textContent`oder `innerText` wenn ich etwas reinschreibe wird alles gelöscht
