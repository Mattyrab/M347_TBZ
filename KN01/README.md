# KN01: Docker Grundlagen

## Installation

Container, auf dem das getting-started Image läuft
![docker getting started webpage](<Screenshot 2025-02-21 092523.png>) 

Container im Docker Desktop
![Running Docker Container](<Screenshot 2025-02-21 092544.png>)

## Docker Command Line Interface (CLI)

Docker Version
![docker version cmd](<Screenshot 2025-02-21 094625-1.png>) 

Docker Suche nach Ubuntu und nginx.
![docker search nginx](<Screenshot 2025-02-21 094650-1.png>) 
![docker search ubuntu](<Screenshot 2025-02-21 094702-1.png>)

`docker run -d -p 80:80 docker/getting-started`

- `docker run`: Neue Container erstellen und starten
- `-d`: Kürz für „detach“ (abtrennen) und führt den Container im Hintergrund aus (Daemon-Modus)
- `-p 80:80`: Verknüpft Ports zwischen dem Host und dem Container. Der erste "80" ist der Host-Port und der zweite "80" ist der Container-Port
- `docker/getting-started`: Der Name des auszuführenden Docker-Images. "docker" ist die Organisation/Benutzername
"getting-started" ist der Name des Repository/Images.

Docker Container mit nginx drauf
![nginx from running container](<Screenshot 2025-02-21 102030.png>)

Mit der Befehl `docker run -d ubuntu` wird zuerst gesucht, ob es eine lokale ubuntu Image gibt. Wenn nicht, dann wird es automatisch heruntergeladen.

Danach wird der Container abgetrennt von der CLI gestartet. Da der start Befehl innerhalb der Container `/bin/bash` ist und weil das abgetrennt gestartet ist, endet der Prozess und der Container wird gleich abgefahren.


Mit der Befehl `docker run -it ubuntu` wird zuerst gesucht, wie der vorherige Befehl, ob es eine lokale ubuntu Image gibt. Da es jetzt schon eine gibt wird diese auch verwendet.

Mit der `-i` Parameter, kurz für „interaktiv“, wird der STDIN offen gehalten (erlaubt die Eingabe von Befehlen).
Der `-t` Parameter weist ein Pseudo-TTY (Terminal) zu, so dass Sie eine Kommandozeile im Container erhalten.

Damit kann man mit dem Container über eine Befehlszeilenschnittstelle interagieren.

Status von Nginx innerhalb der Container prüfen
![nginx status](<Screenshot 2025-02-21 104045-1.png>)

Container Status überprüfen
![container status](<Screenshot 2025-02-21 104304-1.png>)

nginx Container anhalten
![stop nginx container](<Screenshot 2025-02-21 104355-1.png>)

Ubuntu und nginx Containers entfernen
![remove ubuntu and nginx containers](<Screenshot 2025-02-21 104553-1.png>)

Ubuntu und nginx Images entfernen
![remove ubuntu and nginx images](<Screenshot 2025-02-21 104630-1.png>)

## Registry und Repository

Docker Hub Repository
![Remote Repository](<Screenshot 2025-02-21 110322.png>)

## Privates Repository

Ausgeführte Befehle:  
`docker pull ubuntu`  
`docker pull nginx`  
`docker tag nginx:latest mattytbz/m347:nginx`  

- `docker tag`: Neue tag erstellen für eine bestehende Image
- `nginx:latest`: Das zu taggende Image
- `mattytbz/m347:nginx`: Besteht aus drei Teile. Als erstes kommt der Benutzer Name (`mattytbz`), danach der Repo-Name (`m347`), und als letztes der Tag-Name (`:nginx`)

`docker push mattytbz/m347:nginx`  

- `docker push`: Befehl zum Hochladen eines Images in ein remotes Repo
- `mattytbz/m347:nginx`: Besteht aus drei Teile. Als erstes kommt der Benutzer Name (`mattytbz`), danach der Repo-Name (`m347`), und als letztes der Image mit der Tag-Name (`:nginx`)

![image with Tag](<Screenshot 2025-02-21 114302.png>)