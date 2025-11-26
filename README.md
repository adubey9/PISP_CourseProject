# Reflective XSS Testing Environment Using Docker

## Overview
This project provides a simplified and controlled environment for learning and experimenting with **Reflected Cross-Site Scripting (XSS)** vulnerabilities.  
It is designed for educational use, allowing beginners and students to understand how reflected XSS works, why it occurs, and how web applications can defend against it.

The environment is containerized using **Docker**, enabling safe local testing without affecting any external systems.  
Inside the application, user input is intentionally processed insecurely so learners can observe how reflected payloads behave in the browser and how improper input handling introduces XSS risks.

This project focuses strictly on **harmless learning**, preventing misuse while demonstrating core security concepts such as unescaped output, browser script execution, and basic defensive measures.

---

## Core Components

### • Intentionally Vulnerable Reflective Input Handling
Demonstrates how user-supplied data sent via query parameters or forms is directly reflected back into the page without sanitization.

### • Safe Payload Testing
Allows students to try *harmless* sample payloads and visually observe browser behavior.

### • Dockerized Environment
Ensures all experiments run inside an isolated container, making setup safe and reproducible.

### • Defensive Demonstrations
Includes examples of escaping, encoding, and safer rendering techniques to highlight how vulnerabilities can be mitigated.

---

## Project Structure
bugbounty/
├── assets/ # Static assets used by the web application
├── checks.php # Input handling / validation logic (intentionally insecure)
├── db.php # Local DB mock (if needed for extensions)
├── dev.md # Developer notes and instructions
├── docker-compose.yml # Docker environment setup
├── Dockerfile # Builds the vulnerable XSS testing container
├── Dockerfile-SSTI # (If used) Alternative Dockerfile for SSTI labs
├── includes/ # Shared PHP includes and templates
├── index.php # Main entry point – reflects user input
├── init.php # Initialization and config loader
├── labs/ # Placeholder for additional labs (XSS examples, exercises)
├── set-permissions.sh # Sets file permissions inside the container
├── ssti-labs/ # Additional vulnerability labs (not used for XSS)
└── user-content/ # User-generated content (stored locally)

## Core Components

### **Reflective Input Handling**
The main entry point (`index.php`) takes user input from query parameters and reflects it directly into the HTML response.  
This allows learners to see how unescaped input can be interpreted by the browser.

### **Harmless XSS Payload Testing**
The lab includes only safe, demonstration-level payloads to help users understand XSS behavior without enabling misuse.

### **Dockerized Environment**
The application is fully containerized using a single `Dockerfile` and `docker-compose.yml`, making the lab:
- Easy to set up  
- Easy to reset  
- Completely isolated from the host machine  

### **Modular Lab Layout**
Additional lab files can be added inside the `labs/` folder to expand exercises or include variations of reflected XSS scenarios.

---

## Learning Approach

### **Reflective XSS Demonstration**
1. The user provides input in the URL or form.  
2. The server reflects this input back into the output page.  
3. Because the output is not sanitized, the browser may interpret it as HTML or script.  
4. The user observes how and why reflected XSS occurs.

### **Safe Mode Demonstration (Optional)**
Some included files show safer techniques such as:
- HTML escaping  
- Output encoding  
- Basic input validation  

These allow users to compare **vulnerable vs. secure** behavior.

---

## How to Run the Lab

### **1. Build and Start Using Docker**
```bash
docker-compose up --build

