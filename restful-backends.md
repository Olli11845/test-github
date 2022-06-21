# Restful Backends
## Fetch and Http Requests

es gibt verschiedene APIs

XMLHttpRequest API (auch bekannt unter AJAX)        Client to Server
Fetch API               Client to Server
Websockets              Peer to Peer

Clients to Server- Nur der Browser kann requests senden
Peer to Peer. Browser und Backend gehen in beide Richtungen



### XMLHttpRequest API
ist eventbasiert
weit verbreitet für das Laden von Daten


Fetch API:
ist promisebasiert
aktuell das modernste. Wird genutzt.


## HTTP
Kommunikation zwischen Client und Server <br>
![http request](https://user-images.githubusercontent.com/104325830/173789685-e8079627-8da4-4879-9b28-907500256d13.JPG) <br>

HTTP antwortet unter anderem mit Statuscodes. i d r 3 stellig
1xx Information
2xx Successfull operation
3xx REdirect
4xx Client Error
5xx Server Error


### Fetch API and promises
promises sollen dafür sorgen, dass man den Zeitraum zwischen Anfrage und Antwort überdeckt.

A promise
Pending --> Noch nicht weiter gemacht. in der warteschlange
fulfilled --> erfolgreich durchgeführt
rejected --> hat nicht geklappt


fetch methode gibt automatisch ein promise aus.

<br>![response](https://user-images.githubusercontent.com/104325830/173799377-ffd3cbc6-5701-495a-9f44-e54332081e39.JPG) <br>

um die Ergebnisse dann aufzurufen, wenn die Daten da sind muss die json Methode aufgerufen werden

oder hier vollständig: Erst Laden und dann Daten abrufen:
<br>![erst response dann DAten](https://user-images.githubusercontent.com/104325830/173800018-5791465e-2e54-445d-8589-ebc5942c9661.JPG)
<br>
![fetch Abfrage](https://user-images.githubusercontent.com/104325830/173803016-5c9433d5-88fc-4dbf-bae8-d7c32b56f907.JPG)
<br>

## Introduction to Node.js

wir wollen eine API laufen lassen.

eine laufzeitumgebung. Die uns erlaubt JS außerhalb des Browsers zu nutzen.

node.filename.js

um es zu starten.

zweite Funktion von node:
man kann javascript in node ausführen lassen.


LTS Version von Node benutzen

node hat eingebaute features und außerdem externe.

man kann über node.js kommunizieren mit anderen PCs, Sprachen, Computern etc...






node js.

node --version

nvm use --lts

wechselt auf die lts Version




## Project Setup with Node.js and NPM

Node Package Manager

npmjs.org registry. Dort sind alle Pakete veröffentlicht

Open Source heißt nciht dass man es immer ohne Kosten nutzen kann -> bspw. haben diese teilweise Fehler
teilweise leben viele Open Source Projekte von Spenden.

Lizenzen bei Open Source --> Author should get credit. Vor allem Unternehmen müssen das machen.

`Comparison of licences`
`Guide to open source licenses`


in der Datei package.json wird gespeichert, welche Pakete wir benutzen.

nur diese Datei packen wir in mein Repository. Also nur die Info was wir nutzen nicht den Code selbst mit in Git commiten


`npm init` damit können wir unser Repository um ein Element aus der Bibliothek erweitern.
oder 
`npm init --yes` Standard setup. man wird ncihts gefragt. eine leere package.json wird angelegt


zum Hinzufügen des packages:
npm install <packageName>
  
  das Packet wird zu dependencie
 

dargestellt wird dies natürlich in package.json
  
die node packages liegen in `node_modules`wir müssen diesen ordner für git ignorieren. `.gitignore`. da ja nur unser eigener Code in Git landen soll
  
  aber wichtig: package.json gehört in git
  

wenn jemand dann später mein Projekt nutzen will muss er es klonen und `npm install` befehlen. DAnn werden automatisch alle packages aus der package JSON installiert.
  
  
  npm scripts sind Befehle die man in der package json hinterlegen kann.
  
  
  im ordner
  
  `touch.gitignore`
   und dann in der Datei
  /node_modules/
  
  

  
## REST
  
  Endpoints points sind im Grunde genommen URLs
  
  HTTP Methoden
  
  GET Read Data
  POST creates Data
  PUT Update Data
  Delete delete Data


Get /todos/  --> gibt todos als JSON an
Get/todos/1 --> gibt id 1 zurück


Post erstellt einen eintrag im Backend.

  Put kann Daten im Backed updaten 
    Das Backend gibt die Daten die erstellt wurden immer nochmal zurück


git todo aoi klonen in eine repository von mir
im Ordner npm install --> um open source zu laden
  npm run start
  
  dann läuft diese Api auf meinem Rechner. Konsole muss dafür offen sein
  Stoppen mit Ctrl + C oder schließen
  http://localhost:4730
  
  postman wird genutzt um mit API zu interagieren.
  
  wenn etwas schiefgeht und man es resetten will.
  Stop API Ctrl + C
  
  rm db.json
  <br> 
  
  ![wiederherstellen Postman](https://user-images.githubusercontent.com/104325830/174758450-ecfa29e4-b7ab-4933-8e29-0e3a94a04ecc.JPG)
<br>
  
  
  
  
  
  
  
  
  
  
