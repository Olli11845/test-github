## First Steps with GIT

GIT --> Schritte verfolgen

anderer Name repository > repo oder working Folder

Branch Zeitstarhl --> Am Anfang leer
letzte Speichren auf einem Zeitstrahl ist immer "Head"

git kann für das einzelne Projekt als auch allgemein konfiguriert werden

`git config --help` --> zeigt die Hilfe dür den entsprechenden Befehl an

`git init` --> erstellt neues repo an dem entsprechenden Ort

git branch name geändert auf main

#### Arbeit in first-steps-with-git

`git add` schreibt Änderungen an, welche in den nächstzen Commit sollen. Also welche Dateien sollen geändert werden
`git add *` alle DAteien die geändert wurden ins nächste Commit
`git add *.css` schreibt alle geänderten CSS Dateien auf den Index

`git commit -m "Nachricht"` benötigt eine Nachricht was in diesem Schritt gemacht wurde.
jeder commit bekommt einen hash

**Wichtig:**
falls man mal `git commit` ohne -m, also ohne MEssage speichert `:` und `q!` um wieder rauszukommen

`git log` gibt Commit History an. Andere Darstellung `git log --pretty=oneline`

 Create a README.md in your first-steps-with-git folder - passt
 **? Add a brief description why you do this to your README.md ?**git 
 Commit the README.md as the initial commit (use initial commit as the commit message)
 
 
 
 ## remote repository
 
 Standardmäßig hat ein git keine Verbindung
 `git remote` gibt die vorhandenen Verbindungen an. Bei uns am Anfang keine
 `git remote -v`das gleiche zzgl. "sei gesprächig", also mehr Infos
 
 git initialisieren immer lokal. Dann einmal remote erstellen und verbinden. Immer vom REchner auf github synchronisieren, also nicht auf github ändern
 
 `git remote add <name> <url>` Beispiel für github: git remote add origin git@github.com:userName/repo.git .... Der repo Name auf github muss nciht gleich sein
 
 `git remote add origin https://github.com/Olli11845/git-test.git` = Code aus der Github Beschreibung. ERstellt eine Verbindung
 
 `git push` schiebt von lokal nach Github - Infos fehlen
 `git push -u origin main` schiebt nach github




 
 
 
 
