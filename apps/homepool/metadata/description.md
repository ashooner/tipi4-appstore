# HomePool

HomePool is a self-hosted pool and spa maintenance tracker. Log water measurements, treatments, and maintenance tasks, then use the dashboard and dosage recommendations to keep water chemistry on target.

## Features

- Track multiple pools and spas with chlorine, bromine, or salt sanitizers
- Record measurements, chemical treatments, and recurring maintenance
- Customize water-chemistry targets and treatment products per installation
- Review trends, history, and dosage recommendations
- Share installations with read-only or read-and-log access
- Connect to Home Assistant through the upstream HACS integration
- Install the responsive web interface as a PWA

Your data is stored locally in PostgreSQL. On first launch, create an account in the web interface; the first account becomes the instance administrator.

For Home Assistant setup, install the HomePool integration through HACS and use this app's public URL with `/api` appended as the integration base URL.
