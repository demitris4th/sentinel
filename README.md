# **Sentinel**



A cloud-deployed uptime monitoring platform — built in public, phase by phase, as a portfolio project for cloud/DevOps engineering roles.



##### **Status: In progress**



&#x09;Phase 0 complete (Pi provisioned and hardened), Phase 1 starting (core Python monitor + 	SQLite)



##### **What this is**



Sentinel checks a list of URLs on an interval, tracks uptime and response time over time, and alerts on state changes. It started as a simple Python script and is being built out into a full pipeline: persistent storage, a dashboard, containerization, CI/CD, and cloud deployment via Terraform.



(This section will get more specific as the project takes shape so for now it describes the plan. I will update it once Phase 1 code actually exists.)



##### **Why I built this**



I am very passionate about building and creating projects that strengthen my tech skills. This has been a long-term project I always had plans for but never really moved on with it. But now, it is something I will pursue full-time over the course of 3-4 months (hopefully) since I also have full-time university studies and part-time work to worry about as well. The app itself is really simple and to be honest not as complicated and insane as others since this project focuses more on learning DevOps and Cloud-related skills and the process of implementing different tools



##### **Roadmap**



&#x20;(DONE) Phase 0 - Pi provisioned, SSH hardened, toolchain installed

&#x20;	Phase 1 - Core monitor (Python + SQLite, retry logic, tests)

&#x20;	Phase 2 - systemd service + health endpoint

&#x20;	Phase 3 - Dashboard

&#x20;	Phase 4 - Containerization

&#x20;	Phase 5 - CI/CD

&#x20;	Phase 6 - Cloud deployment (Terraform + AWS)

&#x20;	Phase 7 - Observability (Prometheus/Grafana)

&#x20;	Phase 8 - Portfolio packaging



##### **Tech Stack**



Language: Python

Database: SQLite

Web framework: Flask

Containerization: Docker

CI/CD: GitHub Actions

Infrastructure: Terraform

Cloud: AWS (EC2->ECS)

Observability: Prometheus/Grafana



##### **What I learned**



I'll do a fully conclusive summary of what I learned after this project is finished



Please see DEVLOG.md for the raw day-by-day journey I had while developing sentinel, I swear its fun and not boring at all...

