## 🏗️ Infra Bootstrapping & Secure Provisioning
This repository contains hardened provisioning scripts, templates, and automation routines designed to bootstrap secure infrastructure from day one. Whether you're launching a Linux server, cloud VM, or container host, this repo helps enforce secure-by-default standards.

## 🔐 Why This Exists
In many environments, the most critical security gaps are introduced at the moment of provisioning — default users, open ports, missing logging, or unprotected SSH access. This project aims to reduce those risks through:

Hardened cloud-init templates

Secure user creation scripts

Firewall and audit logging configuration

First-run automation with security baked in

This repo is the prevention phase in my broader security and incident response workflow

## 📦 What’s Included
🐧 linux/
secure-cloud-init.yaml – Cloud-init for hardened Ubuntu/Debian instances

user-bootstrap.sh – Adds non-root user with SSH key and disables password auth

auditd-config.sh – Enables auditd, file watches, and retention settings

ufw-setup.sh – Minimal firewall lockdown with logging

☁️ cloud/
aws-secure-instance.tf – Terraform script to launch a hardened EC2 instance with:

Encrypted volumes

Restricted security group

CloudWatch logging bootstrap

azure-vm-bicep.bicep – Secure VM provisioning with locked-down NSGs

🪟 windows/
defender-hardening.ps1 – Enables ASR rules, tamper protection, and logging

secure-user-config.ps1 – Disables SMBv1, configures local audit policies

📄 docs/
bootstrapping-checklist.md – Step-by-step verification guide

lessons-learned.md – Log of issues encountered and fixed over time

git clone https://github.com/yourname/infra-bootstrap-security.git
cd linux
./user-bootstrap.sh

## 🧠 Ideal Use Cases
Spinning up a new homelab VM securely

Prepping a hardened cloud image for your app

Running first-time setup scripts as part of a DevSecOps workflow

Red-teaming your own infra provisioning process
