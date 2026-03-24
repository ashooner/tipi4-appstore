# Deemix

Deemix is a deezer downloader built from the ashes of Deezloader Remix. It allows you to download music from Deezer with full quality support.

## Features

- Download tracks, albums, artists, and playlists from Deezer
- Supports multiple quality levels: FLAC, MP3 320kbps, MP3 128kbps
- Batch downloading with queue management
- Configurable naming templates for downloaded files
- Built-in metadata tagging (album art, lyrics, etc.)
- Web UI for easy management

## Usage

Access the web interface at the configured port after starting the app.

You will need a valid Deezer account (Free or Premium). A Premium account is required for lossless FLAC and MP3 320kbps quality.

### First-time setup

1. Open the web UI
2. Go to Settings and enter your Deezer ARL token
   - To find your ARL: log into deezer.com, open browser DevTools, go to Application > Cookies and copy the `arl` cookie value
3. Configure your preferred download quality and file naming format
4. Start downloading music

## Storage

Downloaded music is saved to your Runtipi media directory at `media/data/music`.
