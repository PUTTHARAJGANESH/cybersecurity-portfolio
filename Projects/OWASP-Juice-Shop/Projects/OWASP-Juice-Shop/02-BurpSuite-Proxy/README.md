# Burp Suite Proxy Configuration

## Objective

Configure Burp Suite as an intercepting proxy between Firefox and OWASP Juice Shop to capture and inspect HTTP requests.

---

## Lab Environment

* Host OS: Windows 11
* Guest OS: Kali Linux
* Virtualization: VMware / VirtualBox
* Docker
* OWASP Juice Shop
* Burp Suite Community Edition
* Firefox Browser

---

## Prerequisites

* Docker installed and running
* OWASP Juice Shop container running
* Juice Shop accessible at:

```text
http://localhost:3000
```

---

## Steps Performed

1. Started Burp Suite.
2. Created a Temporary Project.
3. Selected **Use Burp Defaults**.
4. Opened Firefox.
5. Configured Firefox to use Burp Suite as a proxy.
6. Enabled request interception in Burp Suite.
7. Refreshed the OWASP Juice Shop application.
8. Captured the first HTTP request.

---

## Firefox Proxy Configuration

| Setting                          | Value     |
| -------------------------------- | --------- |
| HTTP Proxy                       | 127.0.0.1 |
| Port                             | 8080      |
| Use this proxy for all protocols | Enabled   |

---

## Expected Intercepted Request

```http
GET / HTTP/1.1
Host: localhost:3000
```

---

## Learning Outcome

* Understood the purpose of an intercepting proxy.
* Learned how browser traffic flows through Burp Suite.
* Captured the first HTTP request from Firefox.
* Prepared the environment for future Application Security testing.

---

## Screenshots

Add the following screenshots after completing the lab:

* Burp Suite startup screen
* Firefox proxy configuration
* First intercepted HTTP request
