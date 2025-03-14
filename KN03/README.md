# KN03: Eigenes Netzwerk

## Vorbereitung

Netzwerk aufstellen und Containers erstellen
![alt text](<Screenshot 2025-03-07 105604.png>)

IP's überprüfen
![alt text](<Screenshot 2025-03-07 110013.png>)

### Pings von Busybox 1 und 3

![busybox1 pings](<Screenshot 2025-03-07 110656.png>)

![busybox3 pings](<Screenshot 2025-03-07 110837.png>)

### Erkenntnisse von KN03

Die Standard Netzwerk "bridge" besitzt keine interne DNS-Resolver, so dass die Containernamen nicht in die entsprechenden IPs aufgelöst werden.

Die benutzerdefinierte Netzwerk "bridge" verfügt über einen internen DNS-Auflöser, so dass die Containernamen in die entsprechenden IPs aufgelöst werden. Dies funktioniert jedoch nur für Containers innerhalb des benutzerdefinierten Netzwerks

### Erkenntnisse von KN02

KN02 verwendet der Standard Netzwerk "bridge". Um die mit einander zu verbinden, wurde durch der `--link` Parameter bei der `docker run --name kn02web -p 80:80 -d --link kn02db mattytbz/kn02b-web:kn02b-web` Befehl ein Verbindung festgelegt.
