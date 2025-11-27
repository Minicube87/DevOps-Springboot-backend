# Dokumentation

Die CICD Pipeline soll mit dem Java Backend:

- Code aus dem Repo ziehen
- Maven Build (mvn clean package) durchführen
- Unit-Tests laufen lassen
- Artefakt erzeugen (JAR oder WAR)
- Artefakt deployen (z.B. in unserem Falle nur ein "echo")

Die Pipeline nutzt Maven und Maven benutzt als Basis die pom.xml.
*Backend deploy*: JAR/WAR in einen Zielordner schieben oder lokalen Tomcat/Java starten
