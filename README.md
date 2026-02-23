# Microservices Observability Hub

Unified observability platform for Spring Boot microservices using OpenTelemetry, Grafana, Prometheus, and Jaeger with AI-powered anomaly detection.

[![Spring Boot 3.2](https://img.shields.io/badge/Spring--Boot-3.2-6DB33F?style=flat&logo=spring-boot&logoColor=white)](https://spring.io/projects/spring-boot)
[![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-1.30-425CC7?style=flat)](https://opentelemetry.io/)
[![Grafana](https://img.shields.io/badge/Grafana-10.x-F46800?style=flat&logo=grafana&logoColor=white)](https://grafana.com/)
[![Prometheus](https://img.shields.io/badge/Prometheus-2.47-E6522C?style=flat&logo=prometheus&logoColor=white)](https://prometheus.io/)

## Overview

Microservices Observability Hub is a turnkey observability stack that auto-instruments Spring Boot services. It provides distributed tracing via Jaeger/Tempo, metrics aggregation via Prometheus, and unified dashboards in Grafana. An AI layer analyzes trace data to identify latency bottlenecks and surface anomalies before they become incidents.

## Key Features

- **Auto-Instrumentation**: OpenTelemetry Java agent auto-instruments Spring Boot services with zero code changes.
- **Distributed Tracing**: Full request lifecycle tracing across all microservices with Jaeger/Tempo integration.
- **Metrics & Alerting**: Prometheus metrics scraping with Alertmanager rules and PagerDuty integration.
- **AI Root-Cause Analysis**: GPT-4 analysis of anomalous trace patterns to suggest probable root causes.
- **Pre-Built Dashboards**: Grafana dashboards for JVM metrics, API latency percentiles, and service dependency maps.

## Tech Stack

- **Instrumentation**: OpenTelemetry Java SDK/Agent, Micrometer.
- **Backend Storage**: Grafana Tempo (traces), Prometheus (metrics), Loki (logs).
- **Visualization**: Grafana 10.x with custom dashboards.
- **AI Layer**: Python FastAPI service + OpenAI GPT-4 for trace analysis.
- **Deployment**: Docker Compose (local), Helm on AWS EKS (production).

## Project Structure

```text
├── sample-services/       # Instrumented Spring Boot demo services
├── otel-config/           # OpenTelemetry collector configuration
├── grafana-dashboards/    # Pre-built Grafana dashboard JSON
├── ai-analyzer/           # Python FastAPI trace anomaly detection
└── infrastructure/        # Helm charts and Docker Compose
```

## License

MIT License. See [LICENSE](LICENSE) for details.
