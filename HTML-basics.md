# HTML

## Syntax

### Elemtente und Tags

HTML ist aufgebaut aus Elementen

Elemente werden mit Tags geöffnet und geschlossen

`<h1> Diese Klammer öffnet das Tag, drinnen ist der Content und am Ende wird es geschlossen </h1>`


Es gibt auch Tags die nur ein offenes Tag haben "self closing Tag"

Tags können verschachtelt sein. Beliebig tief.

### permitted content

w3c markup validator

prüft ob alle REgeln eingehalten wurden! von html selbst kommen keine Fehlermeldungen, wenn man z.B. verbotenes miteinander verschachtelt


### Comments
Kommentare sind nciht sichtbar
öffnen: <!--
schließen: -->


### Attributes

Elemente können Attribute haben. Diese beeinflussen die ELemente
`<tag attribute="attribute value">`
https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes

## Anatomy of HTML

### Basic Structure

- A doctype
- a html element
- a head element
- a body element


nur ein HTML Dokument in einem HTML Dokument eröffnen! 

im Doktype kann und sollte die Sprache angegeben werden.


**head element**
z.b. Titel und allgemeine Informationen

Das `title` element ist der Titel der gesamten sEite. Es darf nur Text enthalten

Meta Informationen sind Teil des Heads
`meta` Elemente stellen Meta Informationen bereit. Siehe liste Meta Data https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta/name

Beispiel: meta tag. "google-site-verification" 

**body** es kann nur einen body im HTML Dokument geben

## HTML and semantics

Semantic sorgt dafür, dass Menschen und Maschinen es verstehen

Accessability --> Barrierefreiheit. WCAG. nicht nur Blinde, sondern viel weiteres

### SEO
Search engine optimization


## HTML Elements for Document Structure

**Beispiel Zeitung**
Header
Main Content
Articles
-  Title
-  Author
-  Text

Footer

https://devdocs.io/html/


`header` element. Für das Dokument selbst oder nächste strukturierende Element (Ist das erste Innerhalb)
<article>
  <header>
    <h2>My previous Jobs</h2>
  </header>
</article>


**Main Element**
was ist der primäre content unserer Seite.

**aside element**

Inhalt der nur sekundären oder tertiären Rang hat.

**footer element**
beschreibt abschließende Informationen. Wie zum Beispiel eine Fußnote

**nav element**
Stellt navigationshilfen. Verweise oder Hinweise für innerhalb des Dokuments

**article**
repräsentiert TExtzeile, welche in sich geschlossen sinn machen. Semantik. Macht das Thema alleine Sinn?

**section**
Abgrenzung zum Artikel: Section kann nicht für sich alleine stehen. Ein großer Block, der nicht für sich selber stehen kann

**heading elements**
h1 - h6. Größe der Überschriften --> Es sollte nur ein h1 element geben.
Heading levels nicht überspringen

header
main
aside
footer
nav
article
section
headings

## Text Elements

Paragraph fasst kleinere Abschnitte zusammen. Text oder Bilder. <p></p>
Vom Spacing her stehen Paragraphen isoliert

`blockquote`. Erweitertes Zitat anzeigen

`q` Zitat innerhalb eines Absatzes

`strong` markiert Inhalt als wichtig

`em` Textelement es ist wichtig das jetzt zu machen

`i` italic element markiert es als technischen Begriff

`small`kleingedrucktes

abbreviation `abbr` für Abkürzungen oder Akronyme

`br` brake Zeilenumbruch

`adresse` Kontaktinformationen




## Anchors

Verlinkungen an andere Orte (gleiches Dokument, aber auch andere)

`href` um auf andere Seiten zu verlinken

`<a href="contact.html">Contact form</a>`

Links werden standardmäßig im gleiven Tab geöffnet

Um einen anchor zu nutzen müssen bestimmte bereiche benannt sein.

Bsp (oben steht der Link wo man drauf klickt. und unten wo es hingeht)

`<a href="#contact">Contact Form</a>`
`...`
`<article id="contact">`
`<form> ... </form>`
`</article>`



## Lists

können geordnet oder ungeordnet sein
`<li> ... </li>`


<ol type="i">
  oder
<ol type="i" reversed>
  oder
<ol>
  <li>...</li>
  <li>...</li>
  <li>...</li>
</ol>

A type attribute 
a lowercase letters
A for uppercase letters
i lowercase roman numerals
I for uppercase roman numerals
1 for numbers
  
  
  `<ul>` unordered list
   
## generic elements

Design ist kein Teil des HTML Dokuments --> daher braucht man Hilfe
  
for styling purposes
if no semantic element is available

2 generische Elemente
  `div` und `span`
  ** div große Blöcke und span kleine Textteile **  
  
  div ist eine container or flow content
  
  span element is used for generic phrasing content
  
  
  ### div
  
  ein container für Elemente.
  
  
  ### span
  wenn ich einen bestimmten Teil ausschneiden und stylen will
  
  
  
  

  
