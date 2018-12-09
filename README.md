Anwendung: In Browser nur Heizung eintippen, dann wird Heizung.html geladen ud steuert alles über ein node-red Websocket namens /ws/gattool2 und von dort aus zu einem node daemon, welcher gatttool -I gestartet hat.

Installation:
Alles im Verzeichnis ~ installieren, nicht in einem Verzeichnis HEIZUNGSPI, wegen Verwendung von .node-red und .xsessionrc

Daten, die außerhalb des Repository gespeichert werden müssen: 
  
  In /etc/hostname der Hostname "Heizung" ohne die Anführungszeichen.

  Bei Email-Steuerung in Datei Schluessel.txt der Schlüssel, welcher am Anfang einer Antwort-Email stehen muss (am Anfang von msp.payload, msg.topic muss "Re: Heizungsraspberrypi." sein), um die Heizung einzuschalten.

