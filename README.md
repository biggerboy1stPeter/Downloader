
# Telegram Media Downloader Bot 🎥🎵

**A powerful, self-hosted Telegram bot** that lets users download videos and audio from **YouTube, TikTok, Instagram, Twitter/X** (and many more sites via yt-dlp).

- Clean inline buttons interface
- Video quality selection (360p–1080p + Best)
- Audio extraction (MP3 192kbps)
- Playlist support (first 10 items)
- Per-user queue & rate limiting
- Real-time download progress
- TikTok watermark avoidance (best effort)
- Optional cookies.txt for private/age-restricted content
- Temporary file auto-cleanup
- FastAPI keep-alive for free hosting platforms (Render, Railway, Fly.io, ...)

![Bot Demo Screenshot](https://via.placeholder.com/800x400.png?text=Bot+Demo+Screenshot)  

## ✨ Features

- **Supported platforms**: YouTube (incl. Shorts), TikTok, Instagram (Reels/posts), Twitter/X, +1500 other sites via yt-dlp
- **Formats**: Video (MP4) or Audio (MP3)
- **Quality options**: 360p, 480p, 720p, 1080p, Best (may exceed Telegram limit)
- **Limits**: ~48 MB per file (Telegram bot restriction), max 5 items in queue, 45s cooldown
- **Progress bar** with speed & ETA
- **Error handling** with friendly, platform-specific messages
- **Cookies support** → `/cookies` command shows setup guide
- **Playlist detection** → sends first 10 items as media group
- **Production-ready** → asyncio queue, throttling middleware, temp dir cleanup

## 🚀 Quick Start (Docker – Recommended)

1. Clone the repo
   ```bash
   git clone https://github.com/YOUR_USERNAME/telegram-downloader-bot.git
   cd telegram-downloader-bot
	2	Create .env file BOT_TOKEN=123456:ABC-DEF1234ghIkl-zyx57W2v1u123ew11
	3	# Optional: PORT=8000 (for hosting platforms)
	4	
	5	(Optional) Add cookies.txt (Netscape format) next to the script for private Instagram / age-restricted YouTube
	6	Run with Docker Compose docker compose up -d --build
	7	 Or without Docker: pip install -r requirements.txt
	8	python bot.py
	9	
📋 Requirements (non-Docker)
	•	Python 3.10+
	•	FFmpeg (for audio extraction & merging)
pip install aiogram yt-dlp python-dotenv fastapi uvicorn
⚙️ Configuration & Tips
File / Var
Purpose
Default / Note
.env → BOT_TOKEN
Your Telegram bot token from @BotFather
Required
cookies.txt
Netscape-format cookies (export from browser)
Optional – enables private/age-gated content
PORT env
Port for FastAPI keep-alive server
8000
MAX_SINGLE_SIZE_MB
Max file size to send (Telegram ~50 MB limit)
48
RATE_LIMIT_SECONDS
Cooldown between user requests
45
Keep yt-dlp updated!
pip install -U yt-dlp
(YouTube & TikTok frequently change → old versions break)
🛠️ Commands
	•	/start — welcome message + usage
	•	/cookies — check cookie status & setup guide
	•	Just send any supported link → choose Video/Audio → quality
📸 Screenshots
(Add your own screenshots here – very helpful for users!)
	1	Start message
	2	Link received → format buttons
	3	Quality selection (video)
	4	Downloading progress
	5	Successful delivery
⚠️ Legal & Responsibility
This bot is for personal, educational use only. Respect platform terms of service and copyright laws. The author is not responsible for any misuse.
📄 License
MIT License
🙏 Acknowledgments
	•	yt-dlp — the real hero
	•	aiogram — excellent Telegram framework
	•	Community examples & issue threads on GitHub

Made with ❤️ in Abuja, Nigeria Last updated: February 2026 Feel free to ⭐ the repo or open issues/PRs!
### Recommendations before publishing

1. **Add real screenshots**  
   Take 4–6 clean Telegram chat screenshots (start → buttons → progress → result)  
   Upload them to repo → replace placeholder links

2. **Create requirements.txt**
   ```txt
   aiogram>=3.0
   yt-dlp
   python-dotenv
   fastapi
   uvicorn
	3	Add LICENSE file (MIT is common) MIT License
	4	
	5	Copyright (c) 2026 Mathias
	6	
	7	Permission is hereby granted, free of charge, to any person obtaining a copy...
