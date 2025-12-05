# Funeral Service Website - In Memory

A respectful and elegant memorial website for funeral services, featuring the complete Order of Service, photo galleries, and video tributes.

## Features

- **Complete Order of Service** with all 15 sections organized and numbered
- **Photo Gallery** for cherished memories
- **Video Support** for tributes and eulogy recordings
- **YouTube Integration** for embedded hymns and music
- **Responsive Design** that works on all devices
- **Print-Friendly** layout for physical programs
- **Elegant Styling** with a respectful, dignified design

## Setup Instructions

### 1. Add Your Content

#### Update Names and Dates
Edit `index.html` and replace all placeholder text marked with `[brackets]`:
- `[Name of Deceased]`
- `[Birth Date] - [Passing Date]`
- `[Officiant's Name]`
- `[Husband's Name]`
- `[Children's Names / Siblings / Close Family]`
- `[Cemetery Name]`
- Service date and location in the footer

#### Add Photos

1. Create an `images` folder in your project:
   ```
   mkdir images
   ```

2. Add your photos to the `images` folder:
   - Main memorial photo: `images/memorial-photo.jpg`
   - Gallery photos: `images/photo1.jpg`, `images/photo2.jpg`, etc.

3. The photos are already referenced in the HTML. Add more gallery items by copying this code in the photo gallery section:
   ```html
   <div class="gallery-item">
       <img src="images/photoX.jpg" alt="Memory description">
   </div>
   ```

#### Add Videos

##### Option 1: YouTube Videos
1. Find the YouTube video URL (e.g., `https://www.youtube.com/watch?v=VIDEO_ID`)
2. Replace `VIDEO_ID` in the embed code:
   ```html
   <iframe src="https://www.youtube.com/embed/VIDEO_ID" frameborder="0" allowfullscreen></iframe>
   ```
3. Uncomment the YouTube embed sections in the HTML where you want videos to appear

##### Option 2: Local Video Files
1. Create a `videos` folder:
   ```
   mkdir videos
   ```

2. Add your video files (MP4 format recommended)

3. Uncomment and use this code:
   ```html
   <div class="video-item">
       <video controls>
           <source src="videos/your-video.mp4" type="video/mp4">
           Your browser does not support the video tag.
       </video>
       <p class="video-caption">Video description</p>
   </div>
   ```

### 2. Test Locally

Open `index.html` in your web browser to preview the website.

### 3. Deploy to Netlify

#### Method 1: Drag and Drop (Easiest)

1. Go to [Netlify](https://app.netlify.com/)
2. Sign up or log in
3. Drag and drop your entire project folder onto the Netlify dashboard
4. Your site will be live in seconds!

#### Method 2: GitHub Integration (Recommended for Updates)

1. **Initialize Git and Push to GitHub:**
   ```bash
   git init
   git add .
   git commit -m "Initial commit - Funeral service website"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/inmemorydivina.git
   git push -u origin main
   ```

2. **Connect to Netlify:**
   - Go to [Netlify](https://app.netlify.com/)
   - Click "Add new site" → "Import an existing project"
   - Choose "GitHub" and select your repository
   - Netlify will auto-detect settings from `netlify.toml`
   - Click "Deploy site"

3. **Your site is now live!** Netlify will provide a URL like `https://your-site-name.netlify.app`

#### Method 3: Netlify CLI

1. Install Netlify CLI:
   ```bash
   npm install -g netlify-cli
   ```

2. Deploy:
   ```bash
   netlify deploy
   ```

3. Follow the prompts to authorize and deploy

### 4. Customize Your Site URL

In Netlify dashboard:
1. Go to "Site settings" → "Site information"
2. Click "Change site name"
3. Enter a memorable name like `inmemory-yourname`
4. Your URL becomes `https://inmemory-yourname.netlify.app`

## Customization Guide

### Change Colors

Edit `styles.css` to change the color scheme:
- **Gold accent**: Search for `#d4af37` and replace with your preferred color
- **Dark background**: Search for `#2c3e50` and `#34495e`

### Add More Sections

Copy any service section and modify:
```html
<section class="service-section" id="section-X">
    <div class="section-number">X</div>
    <div class="section-content">
        <h3>Section Title</h3>
        <p class="description">Description here</p>
    </div>
</section>
```

### Highlight Important Sections

Add the `highlight` class to make a section stand out:
```html
<section class="service-section highlight" id="section-X">
```

## File Structure

```
inmemorydivina/
├── index.html          # Main website file
├── styles.css          # Styling and design
├── script.js           # Interactive features
├── netlify.toml        # Netlify configuration
├── README.md           # This file
├── images/             # Photo folder (create this)
│   ├── memorial-photo.jpg
│   ├── photo1.jpg
│   └── photo2.jpg
└── videos/             # Video folder (create this, optional)
    └── tribute1.mp4
```

## Tips

1. **Image Optimization**: Compress images before uploading to improve loading speed
   - Use tools like [TinyPNG](https://tinypng.com/) or [ImageOptim](https://imageoptim.com/)

2. **Video Recommendations**:
   - Keep videos under 2 minutes for better loading
   - Use YouTube for longer videos to save bandwidth

3. **Mobile Testing**: Test on phones and tablets before sharing the link

4. **Privacy**: If you want to password-protect the site, use Netlify's built-in password protection (available in site settings)

## Support

For questions about:
- **Netlify deployment**: Check [Netlify Documentation](https://docs.netlify.com/)
- **HTML/CSS editing**: Search for tutorials on basic web development
- **Adding content**: Refer to the sections above

## License

This template is provided as-is for memorial and funeral service use.

---

**Created with love and remembrance**
