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
  
  ### colors
  
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
