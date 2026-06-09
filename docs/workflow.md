# Healthcare IoT Honeypot Monitoring Workflow

## Overview

This document describes the end-to-end workflow of the Healthcare IoT Deception Honeypot Network project.

## Workflow Architecture

Attacker
↓
SSH Connection (Port 2222)
↓
Cowrie Honeypot (Docker Container)
↓
Docker Container Logs
↓
Promtail Log Collector
↓
Loki Log Aggregation System
↓
Grafana Dashboard
↓
Security Monitoring & Analysis

## Workflow Explanation

### Step 1: Attack Simulation

An attacker attempts to connect to the exposed SSH service running on port 2222.

### Step 2: Cowrie Honeypot

Cowrie emulates a fake Linux-based healthcare IoT device and records attacker activities.

### Step 3: Activity Logging

All login attempts, commands executed, and file download attempts are captured in log files.

### Step 4: Log Collection

Promtail continuously monitors Cowrie logs and forwards them to Loki.

### Step 5: Log Aggregation

Loki stores and indexes the collected logs for efficient querying.

### Step 6: Visualization

Grafana retrieves logs from Loki and displays them through monitoring dashboards.

## Monitored Events

* SSH Login Attempts
* Executed Commands
* Session Activity
* Malware Download Attempts
* Unauthorized Access Attempts

## Outcome

The workflow enables real-time monitoring and analysis of attacker behavior targeting a simulated healthcare IoT environment.
