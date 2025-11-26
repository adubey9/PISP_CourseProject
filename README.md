# DOM XSS Testing Environment Using Docker

## Overview

This project provides a simplified and controlled environment for learning and experimenting with **DOM-Based Cross-Site Scripting (XSS)** vulnerabilities.  
It is designed for educational use, allowing beginners and students to understand how DOM XSS works, why it occurs in client-side JavaScript, and how insecure DOM manipulation can introduce security risks.

The environment is fully containerized using Docker, enabling safe local testing without affecting any external systems.  
Inside the application, JavaScript intentionally processes user input insecurely so learners can observe how DOM-based payloads execute in the browser and how improper client-side handling leads to XSS.

This project focuses strictly on harmless learning, demonstrating concepts such as insecure DOM sinks, unsafe client-side rendering, and basic defensive techniques.

---
### **• Safe Payload Testing**  
Allows learners to try harmless payloads and visually observe DOM XSS execution.

---

### **• Dockerized Environment**  
The application is fully containerized, making the lab:

- Safe  
- Easy to set up  
- Easy to reset  
- Completely isolated from the host machine  

---

##  Installation Guide

Follow the steps below to install Docker, Docker Compose, and run the DOM XSS testing environment.

---

##  Install Docker (docker.io)

### Ubuntu / Debian
```bash
sudo apt update
sudo apt install -y docker.io
sudo apt install docker-compose
```

## Download the zip file and cd into the directory

```bash
cd bugbounty
```

Start the Docker environment:

```bash
docker-compose up
```

Once the containers are running, open your browser and visit:

```text
http://localhost:80
```

### Approach
In Lab 1 I did DOM Based XSS where I tried `<image src=x onerror="prompt(1)">` and `<img src=x onerror="window.location.href='https://youtube.com'">`

## References
* **TCM Security** - [https://tcm-sec.com](https://tcm-sec.com)
  * Special thanks to TCM Security for providing the learning resources and lab files for this project.




