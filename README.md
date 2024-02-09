This repo contains:

•	3 Dockerized Flask apps on different ports
•	StatsD-Exporter : Collects custom metrics
•	Prometheus: Pre-Configured to scrape from StatsD
•	Grafana : Visualize metrics

Instalaltion :
1.	Clone this repo : https://github.com/sysco999/guicorn_monitoring_statsd.git
2.	Cd guicorn_monitoring_statsd
3.	Run Docker Compose: sudo docker compose up
4.	Run Docker Ps to see the running machines

Troubleshooting :

If the dockerfile isn’t loading check :
•	the CMD commande.
•	The ports (8000 – 8001 -8002 – 9102 – 9090)

If everything goes well, you will be able to access all the created machines for the browser :
-	ip : 8000 === App 1
-	ip : 8001 === App 2
-	ip : 8002 === App 3
-	ip : 3000 === Grafana
-	ip : 9102 === StatsD Exporter
-	ip : 9090 === Prometheus

Script:

use : Python script.py to load the scrips that will start sending requests to the Flask App, this will generate metrics, Prometheus will scape it and it will be shown in the included Grafana Dashboard.
