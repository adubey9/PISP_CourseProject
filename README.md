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
