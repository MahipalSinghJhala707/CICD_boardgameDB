# 🚀 CI/CD Pipeline Automation – Mahipal Singh Jhala

This project implements a complete CI/CD pipeline using Jenkins, Docker, Trivy, SonarQube, Kubernetes, Prometheus, and Grafana on AWS EC2. It automates the entire workflow from code commit to container deployment with integrated testing, security scanning, and monitoring.

---

## 📐 Architecture

| Instance | Services |
|----------|----------|
| 1        | Jenkins, Maven, SonarQube (Docker), Trivy, Node Exporter |
| 2        | Kubernetes Master Node |
| 3        | Kubernetes Worker Node |
| 4        | Prometheus, Grafana, Blackbox Exporter |

---

## 🔁 Pipeline Workflow

1. Code pushed to GitHub → triggers Jenkins pipeline via webhook
2. Jenkins stages:
   - Git checkout
   - Maven build & unit tests
   - Trivy vulnerability scan
   - SonarQube code quality check
   - Docker image build & push
   - Kubernetes deployment
3. Monitoring via Grafana + Prometheus
4. Email notification on build success/failure

---

## 📂 Project Files

- `Jenkinsfile`: Defines all pipeline stages
- `Dockerfile`: For building the app container
- `manifests/`: Kubernetes deployment and service YAMLs
- `prometheus/`: Prometheus and exporter config files
- `trivy-reports/`: Trivy scan reports and summaries
- `screenshots/`: Pipeline execution screenshots

---

## 🔒 Trivy Report Summary

Example output:

| Vulnerability ID | Severity | Package | Installed | Fixed | Description |
|------------------|----------|---------|-----------|-------|-------------|
| CVE-2021-12345   | HIGH     | openssl | 1.1.1f    | 1.1.1g| Buffer overflow issue |
| CVE-2022-67890   | MEDIUM   | curl    | 7.58.0    | 7.64.0| Insecure redirect handling |

Full report available in `trivy-reports/trivy-report.json`

---

## 📊 Monitoring Dashboards

- Prometheus collects metrics from Jenkins, Kubernetes, Node Exporter, and Blackbox Exporter
- Grafana displays:
  - Jenkins build stats
  - Node and pod resource usage
  - Uptime/availability checks via Blackbox

---

## 📸 Screenshots

Refer to the `screenshots/` folder for:
- Jenkins pipeline execution
- Trivy scan results
- SonarQube quality gate
- Prometheus targets
- Grafana dashboards

---

## 🧠 Learnings

- CI/CD orchestration using Jenkins pipelines
- Securing Docker builds using Trivy
- Code quality automation using SonarQube
- Deploying apps on Kubernetes clusters
- Infrastructure monitoring with Prometheus & Grafana

---

## 👨‍💻 Author

**Mahipal Singh Jhala**  
📧 mahipalsinghjhala707@gmail.com  
🔗 [GitHub](https://github.com/MahipalSinghJhala707)
