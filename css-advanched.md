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



