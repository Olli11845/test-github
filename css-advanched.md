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

