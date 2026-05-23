# Jemal A. — DevOps Home Lab Portfolio

Production-grade DevOps home lab built on Hyper-V + Ubuntu 22.04 VM.
Every project solves a real problem, hits real obstacles, and documents
the solution. No tutorials followed — everything debugged from scratch.

---

## Project 1 — End-to-end CI/CD pipeline

**Stack:** Gitea · Jenkins · Docker · Python/Flask · pytest  
**Problem solved:** Manual deployments are slow and error-prone.  
**What I built:** Every git push automatically tests, builds a Docker
image, and deploys — zero manual steps. Full pipeline in 34 seconds.  
**Real problems debugged:**
- Jenkins CSRF blocked webhooks — solved with notifyCommit token
- Docker-in-Docker needed CLI installed separately inside Jenkins container
- Gitea blocked private IP webhooks — fixed with ALLOWED_HOST_LIST config
- Branch mismatch master vs main — common real-world gotcha

**Demo:** [Watch 5-minute Loom](PASTE_LOOM_LINK_HERE)  
**Code:** https://github.com/Jemal-DevOps/my-app

---

## Project 2 — Infrastructure as Code

**Stack:** Terraform · Ansible · Docker · Nginx · Flask  
**Problem solved:** Manually configured servers are unrepeatable and fragile.  
**What I built:** Two servers provisioned by Terraform and configured
by Ansible — identical, automated, idempotent. Full rebuild in under 5 minutes.  
**Real problems debugged:**
- Docker containers have no systemd — replaced with nohup process management
- Ansible Jinja2 conflicts with Python f-strings — separated code into files/
- Resource exhaustion caused silent apt failures — diagnosed with docker stats

**Demo:** [Watch 5-minute Loom](PASTE_LOOM_LINK_HERE)  
**Code:** https://github.com/Jemal-DevOps/iac-project

---

## Project 3 — Observability stack

**Stack:** Prometheus · Grafana · Kubernetes · Helm · Flask metrics  
**Problem solved:** Running software without monitoring means finding
out about problems from users, not dashboards.  
**What I built:** Full RED method monitoring — Request rate, Error rate,
Duration. Alert rule detects incidents in under 2 minutes. Post-mortem
documents the full incident lifecycle.  
**Real problems debugged:**
- Prometheus scraping app outside k8s — additionalScrapeConfigs secret
- Grafana no data — wrong label selector app= vs job= in PromQL
- Port-forwards not surviving reboots — documented recovery procedure

**Demo:** [Watch 5-minute Loom](PASTE_LOOM_LINK_HERE)  
**Code:** https://github.com/Jemal-DevOps/my-app

---

## Infrastructure

| Component | Technology |
|---|---|
| Host OS | Windows 11 with Hyper-V |
| VM | Ubuntu 22.04 LTS — static IP |
| Kubernetes | minikube with Docker driver |
| Local Git | Gitea (self-hosted) |
| CI/CD | Jenkins (Docker) |
| Monitoring | Prometheus + Grafana (Helm on k8s) |

## Skills demonstrated

`Terraform` `Ansible` `Docker` `Kubernetes` `Jenkins` `Prometheus`
`Grafana` `Python` `Nginx` `Git` `Linux` `CI/CD` `IaC`
`Observability` `Incident response` `Post-mortems`
