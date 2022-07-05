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
