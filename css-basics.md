# CSS

warum nimmt man eher CSS als Javascript?


wir arbeiten über selector {} --> damit können wir bestimmte Teile des Codes ansprechen

**wichitg** Box und Sizing

wichtig box model. Eigentlich zerschiesst sich die Gesamtgröße bei Änderungen im Inneren. Daher box sizing modul

Every Element besteht aus einer Box Content --> Padding --> Border --> Margin

Beispiel
border: 2px solid red --> beeinflusst die gesamt Border, aber wenn man danach einzelne ändern will, kann ich es mit folgenden überschreiben (shorthand-property)

man kann auch einzelne Dinge ändern
border-width 2px;
border-style: solid;
border-color: red;

margin: 20px
  alle Seiten 20px
margin-right: 30px
  außer rechts da sind es 30px
  
  
box sizing kann auf 2 Methoden gemacht werden. Eine ist deutlich besser: content-box und border-box

border box. Box sizing bezieht sich auf die gesamte Border box inkl content padding und Border
content box: Das box sizing bezieht sich nur auf den Content

Daher oben drüber: `* (universial selector) 
{box-sizing: border-box;
}`



### CSS und HTML verbinden
1. CSS als externe Quelle --> hauptsächlich genutzt
    im Head: <link rel="stylesheet" href="style.css">
3. CSS inmitten von <style>...Style...</style> -- wenn überhaupt für kleine Anpassungen
4.  <body style="Background-color: grey;">
  
  
## Fonts
  font --> schriftart
  SChriftarten werden kategorisiert
  
  font-family property
  ich kann Schriftarten definieren für das ganze Element oder einzelne Elemente
  
  in der Regel laden wir externe Schriftarten. Auf diese Weise wird sichergegangen, dass es auf jedem System funktioniert
  
  man kann die font family spezifisch angeben bsp: Arial
  oder aber man gibt nur eine familie an: serif, sans-serif oder monospace
  
  mehrere fonts oder font familiys können angegeben werden. Wenn es nicht funktioniert wird zur zweiten gesprungen usw. am Ende könnte man eine Familie setzen und dann klappt es sicher
  
  einzelne Schriftarten in " " angeben. familys nicht. 
  
  
  In der regel gestaltet man die ganze website in xy und macht dann später Änderungen
  
  eine mögliche Quelle für externe fonts ist der eigene Webserver oder z.b. Google fonts
  man legt sich die Schriftarten quasi in einen Warenkob und kann diese dann später per Libk oder import in seinen Code bringen
  **das kommt ins Head Tag**
  
  ### basic selectors
   tag selector 
      ich kann in css bespw ale p (paragraphen ansprechen und sagen p{background-colr: red;}
  gleiches gilt z.B. für div
  
  **class selector**
  
  wir können jedem Element klassen zuweisen (in HTML) und dann in CSS sagen, dass alles mit dieser Klasse einen roten Hintergrund bekommt
  
  HTML: <p class="fancy">textABC </p>
  CSS: .fancy{background-color: green;}

  Ein Attribut in HTMl kann mehrere Klassen haben
  
  
  **id selector**
  
  in Css beisppielsweise die gewählte id: c2 ansprechen
  Wichitg: ID nur einfach vergeben
  
  #p2 {background-color: hotpink;}
  
  
  **attribut selector**
  
  css: [alt] "also alle Elemente die ein source Attribut gesetzt haben" { border: 5px solid red;
  }
  
  oder
   css: [alt="phil murray"] "also alle Elemente die ein source Attribut gesetzt haben und phil murray heißen" { border: 5px solid red;
  }
  
  oder
 
   css: [alt="phil murray" i] "also alle Elemente die ein source Attribut gesetzt haben und phil murray heißen" { border: 5px solid red;
  }  **das i hebelt die groß und kleinschreibung aus**
  
  
  wenn mein Element mit der zeichenkette anfängt
  
  [href^="mailto"] {color: red;
  }
  
  wenn mein Element "google"enthält"
  [href*="google"] {color: red;
    }
  
  
  
  wenn mein Element aufhört mit ".pdf"
  [href$=".pdf"] {font size: 30px;
    }
  
  
  **universal selector**
  `*`
  
  *{border: 5px solid red;
  }
  
  man kann selectoren auch mit komma auflisten
  
  h1, p {background color: hotpink;
    ]
  
  ## colors
  
  können als RGB RGBA oder RRGGBB RRGGBBAA angesehen werden. Rot gelb grün grün und transparent
  außerdem gibt es Vorlagen
  
  Special keywords
  `transparend`--- setz den Block auf durchsichtig 
  `current color` entspricht der aktuell gesetzten Schriftfarbe
  
  background standardmäßig transparent, außer beim dokument. da ist es wei´ß
  
  
  
  currentcolor --> bezieht sich auf eine andere Stelle

  main {
  color: salmon;
  border: 5px solid currentColor;
}
  
  
  ## selector combinators
  
  kombiniert mehrere Selektoren. und können so Dinge abfragen
  
  **descendend combinator**
  Selectoren sind mit leerzeichen getrennt
  beispiel
  `main div { }` --> suche alle divs die im main sind.
  
  
  **child kombinator**
   `main > div` alle divs die **direkte** Kinder von main sind werden ausgewählt. Wenn das div bspw. noch in einem article ist wird es nicht angesprochen
  
  
  **Adjacent Sibling combinator**  Angrenzender Geschwister Kombinator
  
  `main+div` wähle alle div's aus, welche nach dem main kommen.
  
  Geschwisterelement bedeutet, dass es die gleiche ebene ist
  
  
  **General Sibling Combinator**
 
  `main ~ div` --> das div wird angesprochen wenn es ein Geschwisterelement, also ein Element auf gleicher ebene hat. in diesem Fall gefragt nach main
  
  
  **lobotomized owl selector**
  
  `* + *` https://alistapart.com/article/axiomatic-css-and-lobotomized-owls/
  
  spreche alle Elemente außer dem ersten an. Bsp `li* + *li { margin to: 20px;} fügt eine margin top von 20 ein, aber nicht über dem ersten Element.
  
  
  **Pseudo Klassen**
  
  
  pseudo classen
  :first-child erst Element unter zwillingen
  :last-child 
  :only-child
  
  Beispiel Liste. Das first child ist der erste Element der Liste. Weil Child ist das kind der Liste, also das ELement der Liste
  
  
  only child nur dann wenn die Liste nur ein Kind hat. Also eine Liste mit einem Element wird angegsprochen.
  
  child ist immer das Unterelement von Liste. Beispiel. Das child einer Liste ist das element einer liste
  
  
  
  
  :nth-child(n) --> select dthe nth child. zB 1 oder 3
  
  
  Liste pseudo classes
  
  https://developer.mozilla.org/de/docs/Web/CSS/Pseudo-classes
  
  
  
  
  ### pseudo elements
  
  müssen erst aktiviert werden
  
  `::before`
  `::after`
  
  `h1::before {content: 'Herzzeichen'` } dann kommt vor dem h1 ein Herz
  
  `::first-letter` erstes Zeichen kann verändert werden. z.b. font-site 400%
  
  `::first-line` die erste Zeile wird verändet
  
  `::selection` wie soll eine Auswal aussehen. Beispiel Background Color green

  
  ## CSS Cascade
  
Cascade definiert welche Styles auf den Elementen angesprochen werden, wenn es Dopplungen gibt. 
legt Importance, Specify und Origin fest.

  `!important` erhöht die Wichtigkeit. Am ende eines styles
  kann mit einem anderen important quasi überschrieben werden
  
  darunter steht wie spezifisch etwas ist. je spezifischer desto höherwertiger
  
  bei gleicher spezifität --> dann das was als letztes kommt
  
  
  reihenfolge spezifisch, `*`; Tag selectoren: `p`or `div` ; class selectoren .nav oder .main-content ; Attribut Selektroren [title] or [href] ; pseudo classes :hover oder :focus ; Inline styles main style="color:red">  </main>
  
  
  ### Inheritance
  
  ist nicht Teil der Kaskade, aber beeinflusst diese.
  
  beschreibt was für ein property Value genutzt wird, wenn keiner gesetzt ist. Bspw schriftfarbe ist von anfang an schwarz.
  vererbte propertys haben mit text zu tun. werden als ao kinder vererbt
  
  border properties nicht
  
`inherit` = man kann sagen vererbe dinge wie zb. Padding, obwohl dies eigentlich nicht der Fall ist
`initial` =  etwas was eigentlich vererbt wird soll nicht vererbt werden
`unset` = man kann alle vererbten Werte in CSS zurücksetzen
Bsp wenn man was eigenes bauen will, ohn eaufvorgefertigtes zurückzugreifen. `all:unset`
  

  
  ### reset normalize and fallback
  
  Thema: Konflikte mit Browsern
  
  **reset.css**
  z.b. die meisten Werte werden zurückgesetzt auf 0
  Viele Framworks machen das so
  code in den Head dann hat man es resettet
  
  **normalize.css**
  weniger extrem. Standards die keine Probleme verursachen werden beibehalten
  
  **Wichtig wenn eine der beiden Dateien geladen wird muss das im head als erstes passieren, sonst wird es evtl zurückgesetzt**
  
  Fallbacks:
  Zum Bsp für ältere Browser
  Browser ignorieren dinge die sie nciht kennen
  man setzt erst einfache Sachen die immer gehen und überschreibt diese dann mit neuen Dingen (welche ggf noch nicht überall gehen)
  
  logischer Fallback wäre zb dafür zu sorgen , dass die hinterste Background color immer so ist, dass man die SChrift lesen kann, auch wenn bilder o.ä. nicht geladen werden können
  
### Display Block  
`display:block`
`width` `height`

Inline Elements
`Display:Inline`

### Display property and Flow Layout

inline-block > Mischung aus Block und inline Element
inline Block aht im Gegensatz zu inline eine feste Breite



