# 🎵 Pipeband.fun - Pipe Band Trivia Game

A fast-paced trivia quiz that tests your pipe band medley knowledge!

## 🚀 Quick Start

### 1. Configure Cloudinary

1. Create a free account at [cloudinary.com](https://cloudinary.com)
2. Go to your Dashboard and note your **Cloud Name**
3. Go to **Settings > Upload** and create an **Unsigned Upload Preset**:
   - Click "Add upload preset"
   - Set **Signing Mode** to "Unsigned"
   - Name it `pipeband_unsigned`
   - Save

4. Edit `index.html` and replace:
```javascript
const CLOUDINARY_CLOUD_NAME = 'YOUR_CLOUD_NAME'; // Replace with your cloud name
```

### 2. Upload Audio Files to Cloudinary

1. In Cloudinary, go to **Media Library**
2. Create a folder called `pipeband`
3. Upload all MP3 files from the `audio/` folder
4. Rename files to match this format (remove the timestamp prefix):
   - `2012_-_AaronMcLean.mp3`
   - `2012_-_AndrewLawson.mp3`
   - etc.

### 3. Deploy to GitHub Pages

1. Push this repository to GitHub
2. Go to **Settings > Pages**
3. Set Source to "Deploy from a branch"
4. Select `main` branch and `/ (root)` folder
5. Save - your site will be live at `https://yourusername.github.io/pipeband-trivia/`

### Alternative: Deploy to Netlify

1. Push to GitHub
2. Go to [netlify.com](https://netlify.com)
3. Click "Add new site" > "Import an existing project"
4. Connect your GitHub repo
5. Deploy!

## 📁 Project Structure

```
pipeband-trivia/
├── index.html          # Main application
├── README.md           # This file
└── audio/              # Audio files (for reference, upload to Cloudinary)
    ├── 2012_-_AaronMcLean.mp3
    ├── 2012_-_AndrewLawson.mp3
    └── ...
```

## 🎮 Features

- **10 Questions per round** - Random selection from audio library
- **20 seconds per question** - Listen and answer before time runs out!
- **Scoring System**:
  - 3 points for correct band
  - 1 point for correct year
  - Up to 10 bonus points for speed
- **Leaderboard** - Track high scores (stored locally)
- **Facebook Sharing** - Share your score image directly

## ⚙️ Configuration

All configuration is at the top of `index.html`:

```javascript
const CLOUDINARY_CLOUD_NAME = 'your_cloud_name';
const CLOUDINARY_UPLOAD_PRESET = 'pipeband_unsigned';
```

## 📝 Adding More Audio

1. Upload new MP3 files to Cloudinary's `pipeband` folder
2. Add entries to the `audioData` array in `index.html`:

```javascript
{ file: "2015_-_NewBand.mp3", band: "New Band", year: "2015" }
```

## 🔧 Tech Stack

- React 18 (via CDN)
- Vanilla CSS
- Cloudinary (audio hosting + image upload)
- localStorage (leaderboard)

## 📄 License

MIT License - Feel free to use and modify!
