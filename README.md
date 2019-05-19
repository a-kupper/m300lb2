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

Ein kleines Docker-Compose. Gestartet werden ein DB-Server (MariaDB) mit phpMyAdmin und ein Apache-Webserver.
Im phpapache\Dockefile füge ich als erstes einige Extensions hinzu, einfach als proof of conzept. Anschliessend konfiguriere ich Apache usw. und importiere noch ein Zertifikat.
In docker-compose gebe ich noch die geöffneten Ports über das .env-File mit, ebenso wie die Standardkonfigurationsdaten für MySQL.
Obwohl dieses Projektimmernoch relativ klein ist, kam mir nicht wirklich etwas besseres in den Sinn. Ich habe das gefühl, dass man für wirklich umfangreiche Docker-Projekte eine etwas vernünftigere Testumgebung als ein Notebook haben muss.


## Schwierigkeiten

Mit Abstand das grösste Problem war das Zerschiessen meines Arbeits-Notebooks, die fehlenden Backups und der damit verbundene Datenverlust. Bei der Wiederherstellung der Daten konnte ich irgendwie das Image eines kleineren Projektes wiedererlangen, welches ich unterdessen für diese Abgabe verworfen habe.
Schwierigkeiten hatte ich mit diesem Projekt nur insofern, dass Docker für Windows sich anders verhält als Docker über Vagrant und ich mit den Rechten, welche Docker braucht, ein wenig kämpfen musste.


## Fazit

Docker ist ein sehr interessantes und mächtiges Tool welches ich aber noch nicht für meinen Arbeitsalltag einsetzen kann. Ich denke aber, dass dieser Einblick in Container mir sicherlich helfen wird sobald ich mich das nächste Mal mit Docker beschäftigen muss.
