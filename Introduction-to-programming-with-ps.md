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
