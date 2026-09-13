# Media Assets

Place your demo videos, screenshots, and other media files here.

## Folder Structure

```
assets/
├── demo-video.mp4        # Main demo video
├── demo.gif              # Short GIF for README (< 10MB)
├── screenshots/          # Slack conversation screenshots
│   ├── rag-demo.png
│   ├── memory-demo.png
│   └── mcp-demo.png
└── thumbnails/           # Video thumbnails
    └── youtube-thumb.png
```

## File Guidelines

### Videos
- Format: MP4 (H.264)
- Max size: 50MB for GitHub
- Duration: 30-60 seconds
- Resolution: 1920x1080

### GIFs  
- Format: GIF
- Max size: 10MB (GitHub limit)
- Duration: 10-15 seconds
- Use tools like `gifsicle` to optimize

### Screenshots
- Format: PNG
- Resolution: At least 1280x720
- Show actual Slack conversations
- Hide sensitive information

## Optimization

### Video to GIF:
```bash
ffmpeg -i demo.mp4 -vf "fps=10,scale=800:-1:flags=lanczos" -t 10 demo.gif
gifsicle -O3 --colors 256 demo.gif -o demo-optimized.gif
```

### Image Compression:
```bash
# PNG optimization
pngquant --quality=80-95 input.png -o output.png

# Or use online tools:
# - TinyPNG.com
# - Squoosh.app
```
