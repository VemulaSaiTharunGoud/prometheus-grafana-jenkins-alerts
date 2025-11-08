# Prometheus + Grafana + Jenkins — Email Alerts (EC2 + Docker)

This repo contains a complete, easy-to-follow setup to deploy Prometheus, Grafana (with SMTP alerting), Jenkins, and Node Exporter on an Ubuntu EC2 instance using Docker.

**What you get**
- `prometheus.yml` — scrape config for Prometheus (Prometheus, Jenkins, Node Exporter).
- `grafana.ini` — SMTP config for Grafana email alerts.
- `docker-compose.yml` — bring up Prometheus, Grafana, Jenkins, and Node Exporter.
- `setup.sh` — convenience script to prepare the Ubuntu host (install docker, create folders).
- Example: how to create alert rules and folder in Grafana (based on the doc). See original doc for step-by-step instructions. :contentReference[oaicite:1]{index=1}

## Quick start (on Ubuntu EC2)
1. Launch Ubuntu EC2 (t3.large recommended) and open ports: 9090, 3000, 8080, 9100.
2. Clone this repo:
   ```bash
   git clone https://github.com/VemulaSaiTharunGoud/prometheus-grafana-jenkins-alerts.git
   cd prometheus-grafana-jenkins-alerts


Visit:
Jenkins: http://<EC2_IP>:8080 (get initial password via docker exec)
Prometheus: http://<EC2_IP>:9090
Grafana: http://<EC2_IP>:3000
