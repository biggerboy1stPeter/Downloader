# Telegram Media Downloader Bot 🎬🎧📥

<p align="center">
  <a href="https://github.com/biggerboy1stPeter/telegram-media-downloader/stargazers"><img src="https://img.shields.io/github/stars/YOUR_USERNAME/telegram-media-downloader?style=for-the-badge&color=ffd700&logo=github" alt="GitHub stars"></a>
  <a href="https://github.com/biggerboy1stPeter/telegram-media-downloader/forks"><img src="https://img.shields.io/github/forks/YOUR_USERNAME/telegram-media-downloader?style=for-the-badge&color=success&logo=github" alt="GitHub forks"></a>
  <a href="https://github.com/biggerboy1stPeter/telegram-media-downloader/watchers"><img src="https://img.shields.io/github/watchers/YOUR_USERNAME/telegram-media-downloader?style=for-the-badge&color=blueviolet&logo=github" alt="GitHub watchers"></a>
  <a href="https://github.com/biggerboy1stPeter/telegram-media-downloader/releases/latest"><img src="https://img.shields.io/github/v/release/YOUR_USERNAME/telegram-media-downloader?style=for-the-badge&color=ff69b4&logo=github" alt="Latest Release"></a>
  <a href="https://github.com/biggerboy1stPeter/telegram-media-downloader/blob/main/LICENSE"><img src="https://img.shields.io/github/license/YOUR_USERNAME/telegram-media-downloader?style=for-the-badge&color=important" alt="License: MIT"></a>
  <a href="https://github.com/biggerboy1stPeter/telegram-media-downloader"><img src="https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python&logoColor=white" alt="Python 3.10+"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/github/repo-size/biggerboy1stPeter/telegram-media-downloader?style=flat-square&color=9cf" alt="Repo size"> 
  <img src="https://img.shields.io/github/last-commit/biggerboy1stPeter/telegram-media-downloader?style=flat-square&color=9cf" alt="Last commit"> 
  <img src="https://img.shields.io/github/commit-activity/m/biggerboy1stPeter/telegram-media-downloader?style=flat-square&color=9cf" alt="Commit activity">
</p>

**Self-hosted Telegram bot** that downloads videos & audio from  
**YouTube • TikTok • Instagram • Twitter/X** and 1500+ other sites (powered by **yt-dlp**).

Clean inline interface • Quality selector • MP3 extraction • Playlist support • Progress tracking

## 📸 Demo Screenshots

<p align="center">
  <img src="https://via.placeholder.com/320x600/1e293b/ffffff?text=1.+Start+%2F+Welcome+Message" alt="Start message" width="24%">  
  <img src="https://via.placeholder.com/320x600/1e293b/ffffff?text=2.+Link+Received+%26+Format+Buttons" alt="Format selection" width="24%">  
  <img src="https://via.placeholder.com/320x600/1e293b/ffffff?text=3.+Quality+Selection" alt="Quality picker" width="24%">  
  <img src="https://via.placeholder.com/320x600/1e293b/ffffff?text=4.+Downloading+Progress+Bar" alt="Progress bar" width="24%">
</p>


## ✨ Key Features

- **Platforms**: YouTube (incl. Shorts), TikTok (no watermark best-effort), Instagram Reels/Posts, Twitter/X, Facebook, Vimeo + **1500+** sites
- **Output**: Video (MP4) or Audio (MP3 @192kbps)
- **Quality choices**: 360p • 480p • 720p • 1080p • Best available
- **Playlist handling**: Downloads first 10 items as media group/album
- **User limits**: ~48 MB/file (Telegram limit), 5-item queue, 45s cooldown
- **Real-time progress**: ETA, speed, nice progress bar
- **Private content**: Optional `cookies.txt` (Netscape format) support
- **Auto cleanup**: Temporary files deleted after sending
- **Hosting friendly**: FastAPI keep-alive ping (great for free tiers)

## 🚀 Quick Start (Docker – Recommended)

```bash
git clone https://github.com/YOUR_USERNAME/telegram-media-downloader.git
cd telegram-media-downloader

echo "BOT_TOKEN=your_token_here" > .env
# Optional: place cookies.txt here for private content

docker compose up -d --build