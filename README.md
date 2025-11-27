# Dokumentation

Die CICD Pipeline soll mit dem Java Backend:

- Code aus dem Repo ziehen
- Maven Build (mvn clean package) durchführen
- Unit-Tests laufen lassen
- Artefakt erzeugen (JAR oder WAR
- Artefakt deployen (z.B. Testserver)

Die Pipeline nutzt Maven und Maven benutzt als Basis die pom.xml.
*Backend deploy*: JAR/WAR in einen Zielordner schieben oder lokalen Tomcat/Java starten

Die CICD Pipeline soll mit dem npm Frontend:

- Repo clonen
- Node & npm installieren
- Dependencies mit npm install holen
- Test laufen lassen mit (npm test)
- Build erzeugen (npm run build)
- Deployment der Build Files (z.B. /build)

NPM ist der Paketmanager und die CICD Pipeline die Orchestrierung.
*Frontend deploy*: /build Ordner in Testumgebung kopieren oder simplen Webserver starten
