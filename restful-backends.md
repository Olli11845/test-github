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


um die Ergebnisse dann aufzurufen, wenn die Daten da sind muss die json Methode aufgerufen werden

<br>![response](https://user-images.githubusercontent.com/104325830/173799377-ffd3cbc6-5701-495a-9f44-e54332081e39.JPG) <br>
