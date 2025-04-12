
---

# 🎥 GoStreamBridge — RTMP Ingest & Live Transcoding Gateway

> A blazing-fast Go-powered RTMP ingest server that transforms live streams into adaptive HLS output using FFmpeg. Ideal for building your own mini Twitch or live video infrastructure.

---

## 🚀 Project Overview

**GoStreamBridge** is a lightweight and modular **RTMP ingest and HLS transcoding pipeline** written in Go. It allows content creators and developers to stream live video (via OBS, mobile apps, etc.) to a self-hosted server, which then transcodes the stream into multiple resolutions using FFmpeg and serves them over HLS for browser playback.

Perfect for **real-time broadcasting**, **developer live platforms**, **internal event streaming**, or learning how to build a full-stack video pipeline.

---

## 🔧 Features

- 🎬 **RTMP Ingest Server** (powered by [Pion RTMP](https://github.com/pion/rtmp))
- 🎚️ Automatic **transcoding to adaptive bitrates** via FFmpeg (1080p, 720p, 480p, etc.)
- 🧩 Output in **HLS format** (`.m3u8` playlist + `.ts` segments)
- 🌐 **Live stream dashboard**: shows stream metadata, preview, control options
- 🔐 **Stream key authentication** for secure ingest
- 📺 **HTML5 video playback page** using hls.js
- 📊 Real-time stream metrics: bitrate, resolution, latency
- 💾 Local or cloud storage of HLS segments
- ⚙️ Docker-ready for easy deployment

---

## 🧱 Tech Stack

| Component     | Technology         |
|---------------|--------------------|
| Backend       | Go, Pion RTMP, Gorilla Mux / Fiber |
| Transcoding   | FFmpeg (CLI subprocess) |
| Frontend      | Go HTML templates or React/Svelte |
| Playback      | HLS.js or Video.js |
| Storage       | Local filesystem or AWS S3/R2 |
| Database      | SQLite or PostgreSQL |
| Deployment    | Docker, NGINX, systemd, PM2 |



---

## 🚀 How It Works

1. **Stream** from OBS or another RTMP client to your server:
   ```
   rtmp://yourdomain.com/live/streamKey
   ```
2. The Go server receives and parses the RTMP stream.
3. FFmpeg is invoked as a subprocess to transcode the stream to multiple resolutions.
4. Output is segmented into `.ts` files and served via `.m3u8` playlists.
5. Clients view the stream through a modern HLS-compatible player.

---

## 🎯 Use Cases

- Build your own Twitch-style platform
- Host webinars or private live events
- Internal dev/staff livestreaming tool
- Learn about media protocols, transcoding, and Go concurrency

---

## 🛠️ To Do / Roadmap

- [ ] Add WebRTC output (ultra-low latency)
- [ ] Add cloud CDN push for segments
- [ ] Add viewer analytics dashboard
- [ ] Add admin panel for managing users/streams
- [ ] Add mobile streaming client SDK

---

## 🤝 Contributing

Pull requests, feature ideas, and feedback are all welcome!  
Let's build the future of open-source streaming together.

---

## 📜 License

MIT License

---

