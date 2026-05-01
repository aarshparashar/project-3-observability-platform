# Production Observability Platform

A production-grade observability platform demonstrating Site Reliability Engineering (SRE) principles. This project showcases how metrics, structured logs, and distributed traces correlate to provide deep insight into distributed systems, simulating real-world infrastructure scaling and incident response.

## Architecture & Pipelines

1.  **Metrics Pipeline**: Exposes Prometheus-compatible metrics tracking request latency, error rates, queue depths, and CPU/memory saturation.
2.  **Logging Pipeline**: Structured JSON logging with correlation IDs and severity levels. Integrated with log aggregation tools (e.g., Filebeat/ELK stack or Loki) for searching and filtering.
3.  **Tracing Pipeline**: Distributed tracing implementation correlating spans across microservices to identify latency hotspots and trace request paths.
4.  **Dashboarding & Alerting**: Grafana dashboards visualizing system health alongside Alertmanager configurations based on strict Service Level Objectives (SLOs) and error budgets.

## Incident Simulation

A key feature of this repository is the `simulator` module, which deliberately injects faults into the mocked environment:
*   Service crashes
*   Latency spikes
*   Simulated network packet loss
*   Queue backpressure

These simulations trigger the configured alerts and demonstrate how observability tools are used during incident response to quickly diagnose root causes.

## Local Setup

*(Instructions for Docker Compose or Kubernetes manifests will be added here)*
