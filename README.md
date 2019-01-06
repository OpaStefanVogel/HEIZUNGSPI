Anwendung: In Browser nur Heizung eintippen, dann wird Heizung.html geladen ud steuert alles über ein node-red Websocket namens /ws/gattool2 und von dort aus zu einem node daemon, welcher gatttool -I gestartet hat.

Installation:
Alles im Verzeichnis ~ installieren, nicht in einem Verzeichnis HEIZUNGSPI, wegen Verwendung von .node-red und .xsessionrc

Daten, die außerhalb des Repository gespeichert werden müssen: 
  
  In /etc/hostname der Hostname "Heizung" ohne die Anführungszeichen.

  Bei Email-Steuerung in Datei Schluessel.txt der Schlüssel, welcher am Anfang einer Antwort-Email stehen muss (am Anfang von msp.payload, msg.topic muss "Re: Heizungsraspberrypi." sein), um die Heizung einzuschalten.



  server starten mit sudo nred? dann
  
var http = require('http');
 
// Configure our HTTP server to respond with Hello World to all requests.
var server = http.createServer(function (request, response) {
  response.writeHead(301, {"Location": "http://Heizung:1880/Heizung.html"});
  response.end("<html><body>weiter in <a href='http://Heizung:1880/Heizung.html'>Heizung:1880/Heizung.html</a></body></html>");
});
 
// Listen on port 80, IP defaults to 127.0.0.1
server.listen(80);
 
// Put a friendly message on the terminal
console.log("Server running at http://heizung");

