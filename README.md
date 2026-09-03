# Internet Monitoring Stack

A lightweight, self-hosted internet monitoring solution built with Docker, Prometheus, Blackbox Exporter, and Grafana.

This project is designed to monitor internet connectivity, latency, packet loss, and service availability through a simple web-based dashboard.

---

## Overview

The Internet Monitoring Stack provides a local monitoring solution without requiring cloud services, VPS infrastructure, or external monitoring platforms.

The system continuously probes selected network targets and collects monitoring metrics that are visualized through Grafana.

### Main Monitoring Metrics

- Internet availability
- ICMP latency
- Packet loss
- HTTP availability
- Latency history
- Prometheus target health

---

## Architecture

```text
                    INTERNET
                       │
              ┌────────┴────────┐
              │                 │
          Google.com          8.8.8.8
          HTTP Check          ICMP Check
              │                 │
              └────────┬────────┘
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