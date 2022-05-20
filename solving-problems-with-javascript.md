# Solving Problems with Javascript

## pure functions

wiederverwendbare Code ist der beste Code! Im Prinzip sind das pure functions
hat keine Side Effects

Parameter gehen als inout rein 

Return value kommt raus

Falls ich Variablen nach außen verändere ist es keine pure Function

`kopierter Code ist Wurel allen Übels`


## String API essentials
API --> Programing interface

MDN und API anschauen

aufpassen bei groß und kleinschreibung

wichtig: devdocs.io


jede Variable die einen String aufruft kann eine Reihe von BEfehlen ausführen "stringName.Befehle"

Beispiel stringName.includes("was ich suche") --> Ergebnis true oder false. Achtung Case Sensitiv

Beispiel
string.replace("was ich suche","durch was ich es ersetze"); Nur der erste genannte Punkt wird umbenannt.gibt den neuen String zurück. der Alte wird nciht verändert

string.replaceAll("was ich suche","durch was ich es ersetze"); alle gesuchten Objekte werden umbenannt.gibt den neuen String zurück. der Alte wird nciht verändert
string.split(). ich bekomme ein Array zurück. benötigt einen Seperator. Wenn kein Seperator gegeben wird nach jedem Zeichen aufgetrennt


string.IndexOf(" ") sucht einen gegebenen String und gibt die erste Position dieses Strings. Also in diesem Fall Position des ersten Leezeichens
oder suche ab dem ersten Leerzeichen string.indexOf(" ",string.IndexOf(" ")+1)
Wenn das Zeichen nicht enthalten ist kommt "-1" zurück

string.repeat("wie oft wiederholen")  der String wird vervielfacht und neu zurückgegeben.

Casing
string.toLowerCase(); Alle Buchstaben werden klein geschrieben
string.toLowerCase(); Alle Buchstaben werden groß geschrieben


## Callback Functions

1ich kann eine Function zu einer Variable zuweisen. 

function xy() {
console.log("abc") }

const test = xy -- Achtung hier ohne Klammern
nun kann ich die Funktion auch aufrufen indem ich xy() angebe

Anonyme Funktionen
Funktionen ohne Name
const sayHello = function() {
console.log("Hello")
}

sayHello()



function as Parameters. Im Prinzip wie ein Callback funktioniert <br>
![Bild_function_as_parameters](https://user-images.githubusercontent.com/104325830/169482855-4d2d72a7-3589-461c-acee-faed306d0a8c.JPG)
<br>

### Array API Essentials
array.reverse();
array.join();  macht ein array zu einem String. getrennt mit , man kann es auch ändern array.join("-"); so ist der Seperator -
arr.includes(2) <-- ist eine 2 in dem Array enthalten? true oder false
array.forEach() <--
nimmt eine Callback function entgegen für jeden Eintrag des Arrays. kann einen for Loop ersetzen <br>![for_each array](https://user-images.githubusercontent.com/104325830/169485479-7b552a00-9043-4f31-b447-1340d204793e.JPG)
<br>

 
 

array.filter() gibt ein gefiltertes Ergebnis zurück <br>![array filter](https://user-images.githubusercontent.com/104325830/169516017-6cffa433-4f06-4a00-a794-6f0b5c4934a5.JPG)
 <br>
sentence.split(""); ich bekomme jeden Buchstaben einzeln dargelegt. (" ") Seperator ist ein Leerzeichen


array.map() -- wandle etwas um. <br>
![arr map](https://user-images.githubusercontent.com/104325830/169516573-853d663c-b9e8-4aa0-b4be-e8a14fbd2192.JPG) <br>

array.sort() -- findet auf Basis von strings statt. Also wird i Strings gewandelt. **UTF-16 zeichen tabelle!!!!!**
<br>
![arr sort](https://user-images.githubusercontent.com/104325830/169517524-e9408a58-ad1a-43ff-8b36-f924ab2e6343.JPG)
<br>

www.playcode.io









