# Jitsi Meet

Jitsi Meet is a fully encrypted, 100% open source video conferencing solution. No account needed — just share a link and start a meeting.

## Features

- HD audio and video conferencing
- Screen sharing
- Chat during meetings
- Hand raising and reactions
- Recording support (optional)
- End-to-end encryption
- No account required for participants
- Mobile-friendly via browser or native apps

## Setup

### Required

- **Public URL** — the full URL users will use to access Jitsi (e.g. `https://meet.example.com`). This must match exactly — Jitsi uses it for WebRTC signalling.
- **Jicofo Auth Password** — auto-generated on install.
- **JVB Auth Password** — auto-generated on install.

### Behind NAT

If your server is behind NAT (most home/cloud servers), set **JVB Advertise IP** to your server's public IP address. Without this, video will fail to connect for remote participants.

### Ports

Jitsi requires two ports to be reachable from the internet:

| Port | Protocol | Purpose |
|------|----------|---------|
| 8443 | TCP | Web UI (HTTPS) |
| 10000 | UDP | Media (RTP) — must be open in your firewall |

## Services

This app runs four containers:

- **web** — Nginx + Jitsi Meet web interface
- **prosody** — XMPP server for signalling
- **jicofo** — Conference focus / bridge selector
- **jvb** — Jitsi Video Bridge (media relay)
