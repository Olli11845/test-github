# CSS advanched

## flexbox

primär dafür gedacht um Elemente auf begrenztem Raum zu verschieben. 1 Achse

`display:flex` das Element wird zu einem flex container und alle Kinder werden zu flex items. Blocklevel gehen auf die volle breite des eltern elements und zwingen alles danach in die nächste Zeile

`display: inline-flex` fließt über die Zeile hinweg

flex box hat eine haupt und sekundärachse
`flex-direction´
`row´ (ist der Standard) und `row-reverse`möglich

`column` und `column-reverse` 

`justify-content` gibt das Layout auf der Hauptachse an
`justify-conten: space-between` ; space-evenly, space-around, center, flex-start, flex-end


`align-items` gibt das Layout entlang der Hauptachse an. flex-start, flex-end, baseline, center, stretch


order --> grundsätzlich alle Elemente auf 0. Damit können Elemente innerhalb der Flexbox umsortiert werden

`flex-grow` beschreibt wie sich ein element verhalten soll, wenn noch Platz in der Box ist

Beispielsweise hat man 3 Elemente. Eines kriegt eine flex grow 1 und die anderen 2 bzw 0. Dann würde das element  1/3 2/3 bzw 0/3 des Platzes bekommen


`flex-shrink` genau wie grow, aber mit schrumpfen, wenn die box zu klein ist


`flex-basis`setzt die main size von einem Item. Verbunden mit der jeweiligen direction. also länge oder breite
standardmäßig auf auto. Das Element benutzt quasi das was möglich ist


flex 1 2 100px   --> grow, shrink, basis


`align-self` alle ausrichten, aber ein einzelnes Element soll einzeln ausgerichtet sein


`flex-wrap` elemente können umbrechen. Standard: nor wrap aber es gibt wrap oder wrap-reverse


https://css-tricks.com/snippets/css/a-guide-to-flexbox/

Spiel mit Fröschen: https://flexboxfroggy.com/#de


## background images and gradients

background images können gestapelt werden
rgb oder hsl
bzw rgba oder hsla

backround-image und die url funktion url(fileUrl)

verlauf `linear-gradient(25deg,salmon, hotpink)`
z.b linear-gradient(red-blue)

Die richtung kommt über Befehle Degrees, Turn(.25turn), Keywords(to right, to left,

color stabs geben das Ende eines Verlaufes an

background-image: linear gradient(salmon 0%, dodgerblue 60%, gold 100%) 

background-size --> contain (originalgröße) und cover (vollständig ausfüllen). das macht Sinn für Bilder

background size --> auto; keep original size


background repeat: (repeat; no repeat(-x oder -y); space; round) wenn es leere Felder gibt wird das Bild wiederholt



background-position-x und background-position-y; top, bottom, left, right, center
shorthand background position: (x) (y)


`background-clip`= border-box, content-box, padding-box  --> worin soll es angezeiugt werden
oder
background-clip:text;


wenn mehrere erst immer alle bilder
bild1
bild2
bild3

wenn man nur eine Angabe macht gilt das für alle. ansonsten als Beispiel:

background repeat
no-repeat, wichtig mit komma getrennt
no-repeat
repeat


gradienten tool: https://cssgradient.io/

https://projects.verou.me/css3patterns/

Übungen:
cssbattle.dev


## custom properties im HTML Selector, also weit oben
präfix 
`--`
html {
--theme-color: black;
}

main {
color var(--theme-color)
}

Man kann also zentrale Werte der Seite verändern

Man kann bspw. für ganze klassen eine Farbe definieren und dann im HTML eine klasse zuordnen

**Einwurf: mehrere Klassen in HTML zuordnen: class:"eins zwei"**


Custom properties werden vererbt


fallback value.
Ich kann sagen: greife auf custom property zu, aber wenn es keine gibt nimm den: var(--text-color, blue)

https://css-tricks.com/a-complete-guide-to-custom-properties/



##Transitions
ux = User Interface

transition = Ein animierter Übergang
das kann getriggert werden von Javascript oder von user action

transition-property < normalerweise benutzt man das
...-duration
-timing
-delay

**.class {
transition: background-color .5s; 
}
also was erändert

**.class:hover {
background-color:salmon;
}
wohin er es ändert
**

`transition-prpoerty` --> welche eigenschaft soll animiert werden!!!

man sollte keine prpoerties ändern die alles zerschießen, width padding etc. außerdem sehr systemlastig

beste performance `òpacity` and `transform`



`transition-duration` standard = 0sek


transition-timing-function --> beschleunigung oder verlangsamung

eease
linear
ease-in
ease-out
ease-in-out
steps

--> cubic-bezier.com


### transform
transform ist das Ziel, während transition der Weg ist

translate, scale, rotate skew

translate(tx, ty, tz) 
oder einzeln
translateX(tx)
translatey(ty
translate z(tz)

absolute Werte verwenden. px em etc. oder prozentwerte. diese beziehen sich dann auf die größe des Elements selbst

rotate(deg)
rotateX(deg)
rotateY(deg)

transform origin ist die mitte des elements


transform origin: x-offset y-offset z-offset

definiert die Mitte um zu sagen an welchem Punkt es ansetzt. Standard: 50% 50% 0

scale funktion. Wie soll eine eleemt skaliert werden. 1 ist Standard. negative WErte drehen
kann gesamt gemacht werden, aber auch einzeln

scale(s)
scale(sx,sy)
scale(sx,sy,sz)
scaleX(s) or scaleY(s)


aufpassen trigger zittern verhindern indem man umliegendes object anspricht
body: hover div{
transform: translateX(10%}
}
In diesem Fall -> wenn man die Maus über den Body hovert wird das div angesprochen und das ausgeführt

recap
transform-origin = setz den fixpoint fest



## CSS Grid

display:grid --> für 2  dimensionale Sachen
besteht aus Zeilen und Spalten

Die kinder werden Zeilen und spaltenweise einsortiert
Grid cell, grid-track(zeile) , grid-line, grid items(Kinderelemente), Grid-area (mehrere Zellen)

**wichtiger Link eingeworfen: https://every-layout.dev/**

`grid-template-columns` wir können spaltenbreiten definieren. % heißt breite des Containers es gibt auch auto

fr unit eine größenangabe. teilt den Rest auf, arbeitet also mit Anteilen

`auto` reduziert den übrigen Platz, wenn der Container zu klein ist. wenn der Container zu groß ist kommt aber eine Scrollbar

`min-content` soll die Box so klein wie möglich machen
`max-content`die Zeile ist breit genug für den content

auch hier möglich
`justify-content` sortiert alle Zellen innerhalb des Grids. Beschreibt quasiwie man mit leerem Platz umgeht

`align-content`
. wie übliche. sekundäre Achse. start, end, center


´grid-template-rows` genauso wie Spalten

wenn zu wenig Spalten für den Content sind rutscht es in Zeilen. Ohen definition so groß wie nötig

für Platz dazwischen. `grid-column-gap` `grid-row-gap`oder shortcut für beide `grid-gap`

was noch fehlt: Named grid areas, span keyword
https://css-tricks.com/snippets/css/complete-guide-grid/
https://cssgridgarden.com/#de

`grid-column-start: 5;` angesprochen wird die 5. Spalte vom sTart aus

#water {
  grid-column-start: 1;
grid-column-end: 4;
}

Das Element water umfasst nun die Zellen 1,1 1,2 1,3 --> meine Schreibweise

#water {
  grid-column-start: 2;
grid-column-end: span 2;
}

Das Element beginnt bei Spalte 2 und hat dann eine Spanne von 2

grid-column: 2/5;
Bedeuete Spalte von bis;


