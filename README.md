# prometheus-dc

1. Create .env file

   Refer to .env.sample. UID does not need to be specified.

2. Install node_exporter on each target server.

   ```bash
   docker run -d  \
      --net="host"  \
      --pid="host" \
      --name=node-exporter \
      --restart=always \
      -v "/:/host:ro,rslave"  \
      quay.io/prometheus/node-exporter:latest  \
      --path.rootfs=/host
   ```

2. Add the target server IP address etc. to prometheus.yml.

3. Launch with compose

   ```bash
   docker compose up -d --build
   ```
