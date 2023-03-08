# Issue Demo

1. Have a tracing backend you can send traces to (a sample is provided with `docker compose up`)
2. Start this project
3. `curl -u user:user localhost:8081`
4. Now check to see the exemplars `curl -u user:user -H 'Accept: application/openmetrics-text; version=1.0.0' localhost:808`/actuator/prometheus | grep trace_id`
5. Notice there are none.