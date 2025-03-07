# KN02: Dockerfile

## Dockerfile I

Baubefehl: `docker build -t mattytbz/kn02a:kn02a .`  
Startbefehl: `docker run -p 80:80/tcp -p -d 80:80/udp mattytbz/kn02a:kn02a`  
Pushbefehl: `docker push mattytbz/kn02a:kn02a`  

Docker Image kn02a
![kn02a Image](<Screenshot 2025-02-28 092456.png>)

Helloworld Seite von kn02a Container
![webpage from kn02a](<Screenshot 2025-02-28 092402.png>)

kn02a Image in der remote Repo
![kn02a Image in the remote Repo](<Screenshot 2025-02-28 092942.png>)

## Dockerfile II

### DB Befehle

`docker build -t mattytbz/kn02b-db:kn02b-db .`  
`docker run -p 3306:3306 -p 80:80 -d mattytbz/kn02b-web:kn02b-web`

### Web Befehle

`docker build -t mattytbz/kn02b-web:kn02b-web .`  
`docker run --name kn02web -p 80:80 -d --link kn02db mattytbz/kn02b-web:kn02b-web`

### Telnet verbindung test

![telnet to db](<Screenshot 2025-03-07 100023.png>)

### info und db Seiten

![info php](<Screenshot 2025-03-07 095129.png>)

![db php](<Screenshot 2025-03-07 095141.png>)
