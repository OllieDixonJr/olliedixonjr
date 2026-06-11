<!--
  GitHub profile README. Lives in the special OllieDixonJr/OllieDixonJr repo,
  so it renders on the profile page at github.com/OllieDixonJr.
-->

# I make Kubernetes security something you can run, not just read about

**Provision a hardened, STIG scanned Kubernetes cluster and dashboard from your browser, right now, at [olliedixonjr.com](https://olliedixonjr.com).** No install, no setup, no waiting.

https://github.com/user-attachments/assets/788efd66-447e-418a-8ab7-310caee91d25

I'm Ollie Dixon, a DevSecOps and Kubernetes Security Specialist at Lockheed Martin. I build and harden Kubernetes platforms, automate the compliance that proves they're secure, and run the whole thing as a live, public demo anyone can sign into.

---

### How the live demo works

A single GitOps driven k3s platform, public through a Cloudflare Tunnel with **zero open ports** to the internet. Sign in through Authelia SSO and it provisions you an isolated cluster and dashboard on demand. The same platform self hosts an AI assistant on local hardware.

```mermaid
flowchart LR
  user["Visitor browser"] -->|"https, zero open ports"| cf["Cloudflare Tunnel"]
  cf --> traefik["Traefik ingress"]
  traefik --> authelia["Authelia SSO"]
  authelia --> k3s["k3s platform"]
  k3s --> prov["Per user cluster + dashboard provisioning"]
  k3s --> ai["Self hosted AI: Ollama and Open WebUI"]
  git["git push"] --> gitops["GitOps reconciliation"] --> k3s
```

---

### Featured project: [KubeSTIG](https://github.com/OllieDixonJr/kubestig)

**Automated DISA Kubernetes STIG scanning that produces CKL output.** A read only Go scanner that evaluates a live Kubernetes cluster against the DISA Kubernetes STIG and emits `.ckl` files, the format STIG Viewer and eMASS consume.

![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![DISA STIG](https://img.shields.io/badge/DISA-Kubernetes%20STIG-5B2C6F?style=flat-square)
![Apache 2.0](https://img.shields.io/badge/License-Apache%202.0-D22128?style=flat-square)

---

### Currently building

- **KubeSTIG:** expanding STIG control coverage and an eMASS friendly export pipeline
- **The public demo:** per user RBAC and stronger isolation for provisioned clusters
- **A write up** of the zero open ports architecture that safely puts a k3s cluster on the public internet

---

### Certifications

![CKA](https://img.shields.io/badge/CKA-Certified%20Kubernetes%20Administrator-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Security+](https://img.shields.io/badge/CompTIA-Security%2B-E2231A?style=for-the-badge&logo=comptia&logoColor=white)
![AWS CCP](https://img.shields.io/badge/AWS-Cloud%20Practitioner-FF9900?style=for-the-badge&logo=amazonwebservices&logoColor=white)

---

### Stack

![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![k3s](https://img.shields.io/badge/k3s-FFC61C?style=flat-square&logo=k3s&logoColor=black)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![Traefik](https://img.shields.io/badge/Traefik-24A1C1?style=flat-square&logo=traefikproxy&logoColor=white)
![Authelia](https://img.shields.io/badge/Authelia-SSO-103366?style=flat-square&logo=authelia&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

---

### Connect
- [olliedixonjr.com](https://olliedixonjr.com)
- [LinkedIn](https://www.linkedin.com/in/olliedixon)
- OllieDixonJr@gmail.com

<sub>Powered by Kubernetes · Deployed via GitOps · Hardened for security.</sub>
