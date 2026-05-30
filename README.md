# WordPress Homelab

Self-hosted WordPress deployment running on a personal Ubuntu homelab using Docker Compose and Cloudflare Tunnel.

## Overview

This project demonstrates how to deploy and publish a WordPress website from a home server without exposing public ports directly to the internet.

The stack uses Docker Compose to orchestrate WordPress and MySQL containers, while Cloudflare Tunnel provides secure public access through a custom domain.

## Technology Stack

* Ubuntu 24.04
* Docker
* Docker Compose
* WordPress
* MySQL 8
* Cloudflare Tunnel
* Git & GitHub

## Architecture

Internet
→ Cloudflare
→ Cloudflare Tunnel
→ Ubuntu Homelab
→ WordPress Container
→ MySQL Container

## Features

* Dockerized WordPress deployment
* Persistent MySQL and WordPress data using Docker Volumes
* Environment variables managed through `.env`
* Cloudflare Tunnel integration
* Custom domain support
* HTTPS access through Cloudflare

## Getting Started

### Clone Repository

```bash
git clone https://github.com/unreferred/rickyandhika-site.git
cd rickyandhika-site
```

### Configure Environment Variables

Copy the example file:

```bash
cp .env.example .env
```

Edit the values inside `.env` as needed.

### Start Containers

```bash
docker compose up -d
```

### Verify Containers

```bash
docker ps
```

## Lessons Learned

During this project I learned:

* Docker container management
* Docker Compose orchestration
* Environment variable management
* Cloudflare Tunnel configuration
* DNS and HTTPS troubleshooting
* Git and GitHub workflow
* Basic homelab operations

## Disclaimer

This repository contains deployment configuration only.

Sensitive files such as `.env`, SSH keys, Cloudflare credentials, and database data are excluded from version control.

