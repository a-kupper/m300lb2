# M300 LB2

## Einleitung

In diesem README sind die relevanten Informationen zu meiner Arbeit bezüglich Docker.

## Inhaltsverzeichnis

* Docker - Die wichtigsten Befehle
* Was habe ich gemacht
* Schwierigkeiten


## Docker - Die wichtigsten Befehle

`docker run`<br>
Startet einen neuen Container
`docker ps`<br>
Zeigt die aktuellen Container<br>
`docker images`<br>
Zeigt die lokalen Images<br>
`docker rm`<br>
Löscht die angegebenen Container<br>
`docker container prune`<br>
Löscht alle nicht aktive Container
`docker rmi`<br>
Löscht die angegebenen Images<br>
`docker start`<br>
Startet gestoppte Container<br>
`docker stop`<br>
Stoppt den Container<br>
`docker kill`<br>
Stoppt den Container ohne wenn und aber<br>
`docker logs`<br>
Container Logs<br>
`docker inspect`<br>
Informationen zu Containern<br>
`docker diff`<br>
Zeigt Änderungen am Dateisystem des Containers<br>
`docker top`<br>
Informationen zu laufendem Prozess im Container<br>

## Was habe ich gemacht

Aus Zeitgründen, auf welche ich später noch genäuer eingehen werde, ist mein Projekt eher ein Projektchen geworden. 
Im grossen und ganzen habe ich einen kleinen Webserver mit einem Python-App aufgesetzt welches zufällige Katzen-Gifs anzeigt. Mit dem Befehl
`docker run -p 8888:5000 a-kupper/webapp`<br>
Starte ich den Container lokal auf Port 5000, erreichbar von aussen über Port 8888. 

Die ausgeführte Konfiguration im Container ging leider beim Ausführen eines Powershell-Skriptes verloren.

## Schwierigkeiten

Mit Abstand das grösste Problem war das Zerschiessen meines Arbeits-Notebooks, die fehlenden Backups und der damit verbundene Datenverlust. Bei der Wiederherstellung der Daten konnte ich irgendwie das Image eines kleineren Projektes wiedererlangen, das gebe ich nun ab.
Leider reichte die Zeit für einen Neustart nicht mehr aus da ich sowohl im Geschäft als auch Privat im Moment mehr als voll ausgelastet bin.
