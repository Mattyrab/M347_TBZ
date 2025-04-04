# KN07: Kubernetes II

## Begriffe und Konzepte erlernen

Pods:  
Ein Pod ist eine Kubernetes-Ressource, die aus einer Gruppe von einem oder mehreren Containern mit gemeinsamem Netzwerk und Speicher besteht.

Replica:  
Der Zweck eines ReplicaSet besteht darin, einen stabilen Serie von replizierter Pods aufrechtzuerhalten, die zu jedem beliebigen Zeitpunkt laufen.

Deployment:  
Ein Deployment verwaltet eine Reihe von Pods zur Ausführung eines Anwendungs-Workloads. Der gewünschte Zustand des Pods wird innerhalb des Deployments beschrieben und der Deployment Controller ändert den aktuellen Zustand in den gewünschten Zustand.

Service:  
Ein Service ist eine Methode zur Darstellung einer Netzwerkanwendung, die als ein oder mehrere Pods ausgeführt wird. Jedes Service-Objekt definiert einen logischen Bereich von Endpunkten (in der Regel handelt es sich bei diesen Endpunkten um Pods) zusammen mit einer Richtlinie, wie diese Pods zugänglich gemacht werden sollen.

Ingress:  
Ingress stellt HTTP- und HTTPS-Routen von außerhalb des Clusters zu Diensten innerhalb des Clusters zur Verfügung. Das Routing des Datenverkehrs wird durch Regeln gesteuert, die in der Ingress-Ressource definiert sind. Man muss zusätzlich ein Ingress-Controller definieren damit der Ingress-Objekt funktionert.

StatfulSet
Ein StatefulSet verwaltet eine Gruppe von Pods und verwaltet eine dauerhafte Identität für 
für jeden dieser Pods. Dies ist nützlich für die Verwaltung von Anwendungen, die 
dauerhaften Speicher oder eine stabile, eindeutige Netzwerkidentität benötigen.

## Demo Projekt

![webapp-service](<Screenshot 2025-04-04 095341.png>)

![mongo-service](<Screenshot 2025-04-04 095536.png>)

Der Webapp-Service ist ein Nodeport typ, im gegensatz zur der Mongo-Service mit typ ClusterIP. Dies bedeutet, das der Mongo-Service nur innerhalb der Cluster zugänglich ist.

