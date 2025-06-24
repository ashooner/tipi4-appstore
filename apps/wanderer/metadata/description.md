# Wanderer

Wanderer is a self-hosted tool for storing and exploring maps and GPX tracks. It combines a PocketBase backend with Meilisearch indexing and a modern Svelte front-end. The default configuration runs three containers (search, db and web) on a shared Docker network.

Configure the `ORIGIN` environment variable to the public URL of your instance to avoid CORS issues. A strong `MEILI_MASTER_KEY` and `POCKETBASE_ENCRYPTION_KEY` should also be set in production.

Use `docker compose up -d` to start the stack. The web interface will then be available on port 3000 by default.
