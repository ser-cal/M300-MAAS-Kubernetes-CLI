[10]: https://chocolatey.org/install
[20]: https://kubernetes.io/de/docs/tasks/tools/install-kubectl/


# M300-MAAS-Kubernetes-CLI 

Dieses Tutorial unterstützt Dich dabei, den eigenen Windows-Client so aufzusetzen, dass anschliessend eine RESTful-Verbindung zum persönlichen MAAS-Kubernetes API-Server besteht. Dieses Setup ermöglicht es, deklarative Scripts an den K8s API-Server (Control Plane, Master-Node) zu übermitteln und so verschiedene K8s-Übungen durchzuführen. 

Diese deklarativen Scripts sind yaml (oder json)-Files und werden mit dem Kommando **kubectl** dem Control Plane (K8s-Server oder auch Master-Node genannt) übergeben.  
Dieses Packet ist per Default noch nicht auf dem System und muss runtergeladen werden (siehe unten)

## Voraussetzungen:
- [Chocolatey][10]: Windows Package-Manager (nicht zwingend)
- [kubectl][20]: Befehlszeilenprogramm, um Anwendungen auf Kubernetes bereitzustellen und zu verwalten

## Kubernetes-CLI (kubectl) installieren mit Chocolatey
Auf [DIESER URL][20] findest Du die Installationsanleitung für div. Betriebssysteme. <br>
Mit **kubectl** können Clusterressourcen überprüft werden, Komponenten erstellt, gelöscht und aktualisiert werden; Man kann den neuen Cluster betrachten; und Beispielanwendungen aufrufen.

Der folgende Screenshot zeigt die Installation auf Windows mit dem Package-Manager [Chocolatey][10]:

> `$ choco inst kubernetes-cli ` _K8s-CLI Package mit Chocolatey installieren_<br>
> `$ kubectl cluster-info  ` _Checken, ob **kubectl** Output generiert (Pfad ok)_ <br>
  ![Screenshot](images/02_install_kubernetes-cli.png) 

Packete die mit Chocolatey installiert werden, werden abgelegt unter: 
```
 C:\ProgramData\chocolatey\lib\
```

**kubectl** liegt in folgendem Verzeichnis:<br>

```
C:\ProgramData\chocolatey\lib\kubernetes-cli\tools
```
...dies für den Fall, dass die **$PATH**-Variable noch ergänzt werden muss (sollte allerdings im Normfall nicht nötig sein)
