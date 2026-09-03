# Internet Monitoring Stack

A lightweight, self-hosted internet monitoring solution built with Docker, Prometheus, Blackbox Exporter, and Grafana.

## Overview

This project monitors internet connectivity and network performance in real time.

The dashboard provides:

- Internet availability
- Network latency
- Packet loss
- Historical latency monitoring
- HTTP and ICMP monitoring

## Architecture

```text
Internet
   │
   ├── Google
   └── 8.8.8.8
        │
        ▼
Blackbox Exporter
        │
        ▼
Prometheus
        │
        ▼
Grafana
        │
        ▼
Monitoring Dashboard
