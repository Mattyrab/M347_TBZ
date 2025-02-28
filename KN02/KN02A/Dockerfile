FROM nginx  
# Erstellen Sie eine neue Build-Stufe aus einem Basis-Image.

WORKDIR /usr/share/nginx/html
COPY ./helloworld.html .
# Kopiert die angegebene Quelle Datei / Verzeichnis (static-html-directory) in das Ziel Datei / Verzeichnis (gesetzt durch WORKDIR, /usr/share/nginx/html)

EXPOSE 80	
# Teilt Docker mit, dass der Container zur Laufzeit an den angegebenen Netzwerkports lauscht, in diese Fall auf Port 80
