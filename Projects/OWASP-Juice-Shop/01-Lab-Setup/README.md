# 01 - Lab Setup

## Objective

Set up OWASP Juice Shop in a local lab environment for web application security testing.

## Lab Environment

- Operating System: Kali Linux
- Virtualization: Oracle VirtualBox
- Container Platform: Docker
- Web Application: OWASP Juice Shop
- Browser: Firefox

## Installation

Verified Docker installation:

```bash
docker --version
```

Checked running containers:

```bash
docker ps
```

Started Juice Shop:

```bash
sudo docker run -d -p 3000:3000 bkimminich/juice-shop
```

## Verification

Opened the application in a browser:

```text
http://localhost:3000
```

The application loaded successfully.

## Skills Learned

- Docker basics
- Running containers
- Port mapping
- Local web application setup
- Preparing a web security lab

## Evidence

See the Screenshots folder for:
- Docker container running
- Juice Shop homepage
