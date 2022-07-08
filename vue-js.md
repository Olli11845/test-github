# Vue.js


Open Source Project

progressiv --> es kann direkt genutzt werden ohne tooling und es kann komplette interfaces aufbauen

reaktiv --> es reagiert auf Veränderungen, weil es einen virtuellen DOM benutzt
Vue ist reaktiv und das bedeutet, dass es automatisch auf Änderungen reagiert. Wenn wir bspw. ein Array darstellen und verändern dieses, wird es automatisch angeplasst


component driven development. Probleme in kleinere Einheiten zerlegen.

wir lernen vue3


## Include
im Script
`src ="https://unpkg.com/vue@next"`

Abfrage ob es funktioniert. 
`vue.version`


Vue Instance ist der Ort wo man den Vue Code schreibt
instance ist immer Kopie einer Vorlage. das Vue Framework ist diesmal unsere Vorlage

Jede Instance braucht Erweiterungen in Vue.
--> Application instance ist der modernere Name für vue instance.


## Options API
Data
DOM
Lifecycle Hooks
Assets
Composition
Miscellaneous

Options API sagt mir wie die BEgrifflichkeiten lauten und wie ich vue benutzen muss.

Verbindung um Dom herstellen. ein Element wird erstellt mit der ID: APP
<br>
![verbindung zum DOM ID App](https://user-images.githubusercontent.com/104325830/177131734-b3be0e10-a3cb-4131-a250-7f074f515f09.JPG)
<br>


Vue instanzen erzeugen
Vue instanzen mit dem DOM verbinden
Dann Prüfung. `data-v-app`
sonst in der Dev Tool.



data properties
local storage

fast alle direktiven in vue fangen mit v- an.


## templates

man kann in templates bspw verschiedene APIs auf gleiche weise darstellen. Daten kommen rein und werden in das Template gepackt

`{{  }}` Achtung: HTML Tags darin werden als Klartext angegeben. GEfahr: Cross Site Scripting


## directives
vue directives sind Attribute in HTML.
immer: `v-"..."`,
daher: `v-text="'Hello World'";

`v-on:click` bei (klick) passiert etwas. 

eigene directiven erstellen. Hier die directive highlight:
darin steht wann das ganze ausgeführt wird. in diesem Fall bei mount.
<br>
![eigene directive erstellen](https://user-images.githubusercontent.com/104325830/177301864-85dff2fd-fc78-495a-8e5d-915795be3188.JPG)
<br>

v-text: stellt Text dar. Vereinfacht Verbindung zu JS
v-html: kann html text annehmen
v-once: rendert nur einmal
v-pre: Text wird nur noch dargestellt. auch {{ }}
v-bind:
v-model: 2 way data binding. Bspw checkbox an etwas binden


### Attribute Binding
Data properties auf HTML Elemente binden

Wichtig Mustach geht nicht. Das geht nicht für Attribute

`v-bind:class="bgcolor"`
`v-bind:src="src`

v-bind merged, also verbindet verschiedenen
<br>
![v-bind](https://user-images.githubusercontent.com/104325830/177355545-cbed5f6f-6597-4452-af6d-0b27e51246ea.JPG)
</br>

Shortcut

v-bind:class="..." --> :class="..."

wenn man in einem String code einbauen will. keine ' ,sondern '`'
<br>

'"`das ist der String ${stringName}`"' in Edit anschauen



special Attribute:
:key
:ref
:is

:id="dieserNameWirdGeholtAusJS"


### class and style binding

class bindung

v-bind:class=
man kann im Array mehrere CSS Klassen hintereinander schreiben. Vue rendert das zu einem String

<br>
![vue classes](https://user-images.githubusercontent.com/104325830/177728186-98ef8b5a-f280-455c-8202-e2eb7c2c9e20.JPG)
<br>

style binding mit object syntax:
<br>
![style attribute cue](https://user-images.githubusercontent.com/104325830/177729140-1288be90-e278-4261-98e0-571a1a5c147d.JPG)
<br>

conditional class rendering:
man kann auch eine CSS Klasse wie folgt benennen. Man greift über Vue auf ein Objekt zu, welches in CSS ist. Der Key des Objektes ist die CSS Klasse und wenn der Wert ein Boolean ist kann man diese Klasse mit true oder false ein oder ausschalten
<br>
![conditional class vue](https://user-images.githubusercontent.com/104325830/177733928-fe783fbf-6208-4dee-9846-2b2973d26477.JPG)
<br>

class binding vue.js
`:class` 


### Vue if

wichtig die in diesem Fall div's müssen aufeinander folgen
<br>
![vue if](https://user-images.githubusercontent.com/104325830/177766741-1cf8cd84-7eb7-4a67-b02b-0c1334e09df9.JPG)
<br>

alternativ um etwas auszublenden
<br>
![v-show](https://user-images.githubusercontent.com/104325830/177766994-98674fd8-e377-4ceb-bee1-144854db87c8.JPG)
<br>

### List rendering

v-bind:key
:key attribute

v-for gilt für `for of` und `for in`
<br>
![v-for](https://user-images.githubusercontent.com/104325830/177814699-777280a6-88b1-4662-9deb-9a4024f12353.JPG)
<br>
ich habe so viele li wie einträge im array


wenn ich eine for Schleife auf einem DIV container mache habe ich danach 10 DIVs
gebraucht wird ein v-bind:key Attribut.



