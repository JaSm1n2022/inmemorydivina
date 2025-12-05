# Video & Audio Embed Guide

## 🎥 YouTube Videos

**Format:**
```html
<iframe src="https://www.youtube.com/embed/VIDEO_ID" frameborder="0" allowfullscreen></iframe>
```

**How to get VIDEO_ID:**
- From URL: `https://www.youtube.com/watch?v=dMFO9n_pUXA`
- VIDEO_ID is: `dMFO9n_pUXA`
- Use: `https://www.youtube.com/embed/dMFO9n_pUXA`

---

## 📘 Facebook Videos

### Method 1: Facebook Embed (Recommended)

**Step 1:** Go to https://developers.facebook.com/docs/plugins/embedded-video-player/

**Step 2:** Paste your Facebook video URL

**Step 3:** Click "Get Code"

**Step 4:** Copy the `<iframe>` code (choose "IFrame" tab)

**Step 5:** Paste into your HTML

### Method 2: Manual Format

**Your Facebook URL:**
```
https://www.facebook.com/jacq.baldoza.avancena.1/videos/740713069067012
```

**Convert to embed format:**
```html
<iframe
    src="https://www.facebook.com/plugins/video.php?href=https%3A%2F%2Fwww.facebook.com%2Fjacq.baldoza.avancena.1%2Fvideos%2F740713069067012&show_text=false&width=560"
    width="560"
    height="315"
    style="border:none;overflow:hidden"
    scrolling="no"
    frameborder="0"
    allowfullscreen="true"
    allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share">
</iframe>
```

### Method 3: Link Button (If video is private/restricted)

```html
<a href="https://www.facebook.com/jacq.baldoza.avancena.1/videos/740713069067012"
   target="_blank"
   class="video-link-button">
    📺 Watch Video on Facebook
</a>
```

**Important:** Facebook videos with privacy restrictions may not embed. In this case, use the link button method.

---

## 🎵 Audio Files (MP3)

**Simple Audio Player:**
```html
<audio controls>
    <source src="audio/filename.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
</audio>
```

**With Autoplay & Loop:**
```html
<audio controls autoplay loop>
    <source src="audio/filename.mp3" type="audio/mpeg">
</audio>
```

**Note:** Most browsers block autoplay unless user has interacted with the page.

---

## 🎬 Local Video Files

**MP4 Video:**
```html
<video controls>
    <source src="videos/filename.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>
```

**With Width Control:**
```html
<video controls style="max-width: 100%;">
    <source src="videos/filename.mp4" type="video/mp4">
</video>
```

**Supported Formats:**
- MP4 (best compatibility)
- WebM
- OGG

---

## 📂 File Organization

```
inmemorydivina/
├── audio/
│   ├── prelude.mp3
│   ├── hymn1.mp3
│   ├── lonely.mp3
│   └── moms-beautiful-angel.mp3
├── videos/
│   ├── tribute1.mp4
│   └── eulogy.mp4
└── images/
    ├── memorial-photo.jpg
    └── photo1.jpg
```

---

## 🔧 Troubleshooting

### YouTube video not showing?
- ✅ Use `/embed/` format, not `/watch?v=`
- ✅ Check video is not private/restricted
- ✅ Make sure VIDEO_ID is correct

### Facebook video not showing?
- ✅ Check video privacy settings (must be Public)
- ✅ Try getting embed code from Facebook Developer tools
- ✅ Use link button as fallback

### Audio not playing?
- ✅ Verify file is in `audio/` folder
- ✅ Check filename matches exactly (case-sensitive)
- ✅ Use MP3 format for best compatibility
- ✅ Include `controls` attribute

### Local video not working?
- ✅ Use MP4 format
- ✅ Verify file is in `videos/` folder
- ✅ Check file size (large files may be slow)
- ✅ Consider using YouTube for large videos

---

## 💡 Tips

1. **YouTube** - Best for long videos, automatic quality adjustment
2. **Facebook** - Use only if video is public, may have embedding restrictions
3. **Local MP3** - Best for short audio clips (under 5MB)
4. **Local MP4** - Use for videos under 50MB, otherwise use YouTube
5. **Privacy** - Remember embedded videos inherit the source's privacy settings

---

## 🎯 Quick Reference

| Media Type | Best Format | Code |
|------------|-------------|------|
| YouTube Video | Embed URL | `<iframe src="https://www.youtube.com/embed/ID">` |
| Facebook Video | Plugin URL | Use Facebook Developer embed tool |
| Audio | MP3 | `<audio controls><source src="audio/file.mp3">` |
| Video | MP4 | `<video controls><source src="videos/file.mp4">` |
| External Link | Button/Link | `<a href="URL" target="_blank">Watch Video</a>` |
