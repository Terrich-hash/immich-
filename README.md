# Self-Hosting Immich on Linux with Tailscale

This repository documents how to self-host **:contentReference[oaicite:0]{index=0}** on a Linux server and securely access it over a private network using **:contentReference[oaicite:1]{index=1}**.

Immich is a high-performance, self-hosted photo and video backup solution similar to Google Photos, but fully private and under your control.

---

## Features

- Self-hosted photo & video backup
- Web and mobile app support
- Face recognition and search
- No public ports exposed
- Access limited to Tailscale network only

---

## Requirements

### Server
- Linux server (Ubuntu / Debian recommended)
- Docker & Docker Compose
- Minimum 4 GB RAM (8 GB recommended)
- SSD storage recommended

### Client Devices
- Tailscale installed
- Immich mobile app (optional)

---

## Install Docker & Docker Compose

```bash
sudo apt update
sudo apt install -y docker.io docker-compose
sudo systemctl enable docker
sudo systemctl start docker

Optional (run Docker without sudo):

sudo usermod -aG docker $USER
newgrp docker
