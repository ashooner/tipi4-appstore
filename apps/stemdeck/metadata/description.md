# StemDeck

StemDeck is a free, self-hosted music stem separator. Import an audio file or a supported media URL to split a song into vocals, drums, bass, guitar, piano, and other stems. The browser interface includes a multitrack mixer, waveform navigation, looping, analysis, and stem or mix export.

## NVIDIA GPU requirement

This app definition is configured for NVIDIA GPU acceleration. Before installing it, the Runtipi host must have:

- A supported NVIDIA GPU and working host driver
- NVIDIA Container Toolkit configured for Docker
- Docker Compose GPU device reservations support

The published StemDeck image already includes CUDA-enabled PyTorch. The app reserves all available NVIDIA GPUs and forces Demucs to use CUDA; no CUDA toolkit needs to be installed inside the container.

StemDeck itself can run on a CPU, but this store definition intentionally requests an NVIDIA GPU. To run it without one, create a Runtipi user override that removes the `deploy.resources.reservations.devices` section and the three GPU-related environment variables (`STEMDECK_DEMUCS_DEVICE`, `NVIDIA_VISIBLE_DEVICES`, and `NVIDIA_DRIVER_CAPABILITIES`). Stem separation will be substantially slower.

Processed tracks and the StemDeck library are stored under `data/jobs`. Model weights and Torch downloads are cached under `data/cache`, so they survive app upgrades. The first separation downloads the model and can take longer than later jobs.

> StemDeck has no user authentication. Avoid exposing it directly to the public internet unless access is protected by an authentication layer.
