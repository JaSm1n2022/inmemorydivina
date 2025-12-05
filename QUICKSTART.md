# Quick Start Guide

## 3 Simple Steps to Get Your Memorial Website Live

### Step 1: Add Your Content (10-15 minutes)

1. **Edit names in `index.html`:**
   - Open `index.html` in any text editor
   - Find and replace all text in `[brackets]` with actual names and information
   - Search for `[Name of Deceased]` and replace throughout

2. **Add photos to `images/` folder:**
   - Add `memorial-photo.jpg` for the main header photo
   - Add `photo1.jpg`, `photo2.jpg`, etc. for the gallery

3. **Add videos (optional):**
   - **For YouTube videos:** Get the video ID from YouTube URL and add to the HTML
   - **For local videos:** Add MP4 files to `videos/` folder

### Step 2: Test Locally (2 minutes)

Simply double-click `index.html` to open in your browser and preview.

### Step 3: Deploy to Netlify (5 minutes)

**Easiest Method - Drag & Drop:**

1. Go to [app.netlify.com](https://app.netlify.com)
2. Sign up (free)
3. Drag your entire project folder onto the page
4. Done! You'll get a live URL instantly

**Alternative - GitHub Method:**

```bash
# In your project folder, run:
git init
git add .
git commit -m "Memorial website"
git remote add origin YOUR_GITHUB_REPO_URL
git push -u origin main

# Then connect GitHub to Netlify at app.netlify.com
```

## Need Help?

### How do I add a YouTube video?

1. Get your YouTube URL: `https://www.youtube.com/watch?v=ABC123`
2. Copy the part after `v=` (that's your VIDEO_ID)
3. In `index.html`, find this commented code and uncomment it:
   ```html
   <!-- <iframe src="https://www.youtube.com/embed/VIDEO_ID" frameborder="0" allowfullscreen></iframe> -->
   ```
4. Replace `VIDEO_ID` with your actual ID:
   ```html
   <iframe src="https://www.youtube.com/embed/ABC123" frameborder="0" allowfullscreen></iframe>
   ```

### How do I add more photos to the gallery?

In the Photo Gallery section of `index.html`, copy and paste this:

```html
<div class="gallery-item">
    <img src="images/photoX.jpg" alt="Description">
</div>
```

Just change `photoX.jpg` to match your photo filename.

### How do I change the colors?

Open `styles.css` and search for:
- `#d4af37` (gold color) - replace with any color code
- `#2c3e50` (dark blue) - the main dark color

### Where do I add scripture text?

Find this section in `index.html`:

```html
<div class="scripture-text">
    <!-- Add actual scripture here -->
</div>
```

Add your text between the div tags.

## Checklist Before Going Live

- [ ] All `[bracketed placeholders]` replaced with real information
- [ ] Memorial photo added to `images/memorial-photo.jpg`
- [ ] Gallery photos added to `images/` folder
- [ ] Service date and location updated in footer
- [ ] Tested by opening `index.html` in browser
- [ ] Videos added (if using)
- [ ] YouTube embeds added (if using)

## Common Issues

**Photos not showing?**
- Check that filenames match exactly (case-sensitive)
- Make sure photos are in the `images/` folder

**Videos not playing?**
- Use MP4 format for best compatibility
- For large videos, use YouTube instead

**Want to password protect?**
- After deploying to Netlify, go to Site Settings → Access Control

---

**Ready to deploy?** Head to [app.netlify.com](https://app.netlify.com) and drag your folder!
