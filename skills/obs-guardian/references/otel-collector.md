# OpenTelemetry Collector Reference

1. Use the Collector as the telemetry gateway between services and backends.
2. Keep receiver, processor, exporter, and service pipeline sections explicit.
3. Prefer OTLP receivers for modern OpenTelemetry SDKs.
4. Add resource attributes for service name, environment, version, and region.
5. Use batch processing to reduce exporter overhead.
6. Use memory limiter processing to protect the Collector under load.
7. Use tail sampling only after understanding trace volume and latency impact.
8. Keep sampling decisions consistent for related services where possible.
9. Do not add user IDs, emails, or request IDs as metric labels.
10. Redact secrets and personal data before telemetry leaves the trust boundary.
11. Separate dev, staging, and production exporters.
12. Validate configs before rollout.
13. Roll out Collector changes gradually when it is shared infrastructure.
14. Monitor Collector CPU, memory, dropped spans, queue size, and exporter errors.
15. Use health check and pprof extensions where appropriate.
16. Prefer secure OTLP endpoints with TLS for production traffic.
17. Document backend ownership and retention for each signal.
18. Keep logs, metrics, and traces joinable with trace ID and service metadata.
19. Use recording rules for expensive Prometheus dashboard queries.
20. Link alert rules to runbooks and dashboards.
21. Treat Collector outages as production visibility incidents.
