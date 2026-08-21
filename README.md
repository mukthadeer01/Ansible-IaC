![Ansible](https://img.shields.io/badge/Ansible-E00F2F?style=for-the-badge&logo=ansible&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

## 📌 Overview
This repository contains Infrastructure as Code (IaC) playbooks and configurations using **Ansible** to automate the provisioning, configuration, and management of cloud-native infrastructure. It is designed to streamline DevOps workflows, reduce manual deployment overhead, and ensure idempotent configuration across multiple worker nodes.

Currently, this repository heavily focuses on automated Docker installation, user group management, and secure container registry authentication across distributed environments.

## 🚀 Features
* **Automated Package Management:** Seamless system updates and dependency installations across target nodes (Ubuntu/Debian/RHEL).
* **Container Runtime Provisioning:** Automated deployment of `docker.io` / `docker-ce`, service state management, and daemon configuration.
* **Identity & Access:** Automated configuration of secondary user groups (e.g., adding users to the `docker` group) to eliminate permission bottlenecks.
* **Idempotent Workflows:** Built with Ansible best practices to ensure playbooks can be run repeatedly without unintended side effects.

## 📂 Repository Structure
```text
📦 Ansible-IaC-DevOps
 ┣ 📂 inventory
 ┃ ┗ 📜 hosts.ini          # Target node IP addresses and groupings
 ┣ 📂 roles
 ┃ ┗ 📂 Docker
 ┃   ┣ 📂 tasks
 ┃   ┃ ┗ 📜 main.yml       # Core tasks for Docker installation & config
 ┃   ┗ 📂 vars
 ┃     ┗ 📜 main.yml       # Variables for users, registry auth, etc.
 ┣ 📜 site.yml             # Master playbook calling the roles
 ┗ 📜 README.md
