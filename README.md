# prometheus-dc

Docker compose files that make metrics from multiple servers available externally through a cloudflare tunnel using prometheus. Prometheus endpoint is assumed to be accessed from Grafana Cloud by setting service auth with Cloudflare Access. You can get a good visualization by using the [`ID: 893`](https://grafana.com/grafana/dashboards/893-main/) dashboard.

## Usage

1. Create .env file

   Refer to .env.sample. UID does not need to be specified.

2. Set up a monitoring target server

   ```bash
   docker compose -f compose.target.yml up -d --build
   ```

3. Add the target server IP address etc. to prometheus.yml.

4. Launch with compose on the monitoring server

   ```bash
   docker compose up -d --build
   ```
