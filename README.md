# prometheus-dc

1. Create .env file

   Refer to .env.sample. UID does not need to be specified.

2. Edit prometheus.yml

3. Launch with compose

   ```bash
   export UID=${UID} docker compose up -d --build
   ```
