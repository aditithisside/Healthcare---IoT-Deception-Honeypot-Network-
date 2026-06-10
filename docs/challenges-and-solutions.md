# Deployment Challenges and Solutions

## Challenge 1: Python 3.13 Compatibility Issue

### Problem

Cowrie honeypot encountered dependency and compatibility issues while running on Python 3.13.

### Solution

Switched from manual installation to Docker-based deployment, which provided a stable and isolated runtime environment.

---

## Challenge 2: SSH Host Key Verification Error

### Problem

After restarting the Cowrie container, SSH connections produced a "REMOTE HOST IDENTIFICATION HAS CHANGED" warning.

### Solution

Removed the old SSH fingerprint from the known_hosts file and re-established the connection.

---

## Challenge 3: Loki and Promtail Port Conflict

### Problem

Promtail failed to start because a required port was already being used by another service.

### Solution

Modified the Promtail configuration and assigned a different listening port.

---

## Challenge 4: Grafana Visualization Error

### Problem

Grafana panels displayed the message "Data is missing a number field".

### Solution

Changed panel visualization from graph-based views to log-based views suitable for textual security logs.

---

## Challenge 5: System Resource Constraints

### Problem

Running Docker, Cowrie, Grafana, Loki, and Promtail simultaneously caused performance issues on the local system.

### Solution

Optimized resource usage by closing unnecessary applications and using lightweight log aggregation components.

---

## Key Learning

These deployment challenges provided practical experience in troubleshooting, log management, Docker deployment, SSH connectivity, and security monitoring infrastructure.
