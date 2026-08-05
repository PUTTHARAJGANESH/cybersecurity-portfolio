# Burp Suite Proxy Configuration

## Objective

The objective of this lab is to configure Burp Suite as an intercepting proxy between Mozilla Firefox and OWASP Juice Shop. This allows HTTP requests and responses to be captured, inspected, and analyzed before they reach the web application.

---

## Introduction

Burp Suite is one of the most widely used tools for Web Application Security Testing. It acts as a proxy between a web browser and a web server, allowing security professionals to inspect, modify, and replay HTTP/HTTPS traffic. Understanding how Burp Suite works is a fundamental skill for Application Security Engineers and Penetration Testers.

---

## Lab Environment

| Component              | Details                      |
| ---------------------- | ---------------------------- |
| Host Operating System  | Windows 11                   |
| Guest Operating System | Kali Linux                   |
| Virtualization         | VMware / VirtualBox          |
| Vulnerable Application | OWASP Juice Shop             |
| Web Browser            | Mozilla Firefox              |
| Proxy Tool             | Burp Suite Community Edition |
| Container Platform     | Docker                       |

---

## Prerequisites

Before starting this lab, ensure the following:

* Docker is installed and running.
* The OWASP Juice Shop container is running.
* Juice Shop is accessible at:

```text
http://localhost:3000
```

---

## Network Flow

```text
Mozilla Firefox
        │
        ▼
Burp Suite (Intercepting Proxy)
        │
        ▼
OWASP Juice Shop
```

---

## Firefox Proxy Configuration

| Setting                          | Value     |
| -------------------------------- | --------- |
| HTTP Proxy                       | 127.0.0.1 |
| Port                             | 8080      |
| Use this proxy for all protocols | Enabled   |

---

## Lab Tasks

During this lab, the following tasks will be completed:

* Launch Burp Suite.
* Create a Temporary Project.
* Use the default Burp configuration.
* Configure Firefox to use Burp Suite as the proxy server.
* Enable request interception.
* Capture the first HTTP request sent to OWASP Juice Shop.
* Understand the structure of an HTTP request.

---

## Expected HTTP Request

```http
GET / HTTP/1.1
Host: localhost:3000
```

---

## Learning Objectives

After completing this lab, I will be able to:

* Explain the purpose of an intercepting proxy.
* Configure a browser to route traffic through Burp Suite.
* Capture and inspect HTTP requests.
* Understand how web requests travel between a browser and a web application.
* Prepare the testing environment for future Application Security assessments.

---

## Screenshots

After completing the practical, the following screenshots will be added:

* Burp Suite startup screen
* Firefox proxy configuration
* First intercepted HTTP request
* Burp Suite Proxy → Intercept tab

---

## Conclusion

This lab establishes the foundation for web application security testing. Configuring Burp Suite correctly is the first step toward analyzing HTTP traffic and performing security assessments such as authentication testing, input validation testing, SQL Injection, Cross-Site Scripting (XSS), and Broken Access Control testing.
