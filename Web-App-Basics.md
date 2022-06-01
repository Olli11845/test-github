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










