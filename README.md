# Life on Marzj - Portfolio Website with AR Experience

This is your personal portfolio website with a hidden AR prison cell experience accessible only via QR code.

## 🌐 Website Structure

```
lifeonmarzj-website/
├── index.html              # Main portfolio homepage
├── robots.txt              # Hides AR page from search engines
├── css/
│   └── style.css          # Main stylesheet
├── js/
│   └── main.js            # Main JavaScript
├── assets/
│   ├── images/            # Your images
│   ├── models/            # 3D models (GLB/GLTF)
│   └── targets/           # AR target images
│       └── prison-cell-marker.mind  # mind-AR compiled target
└── ar-experiences/
    └── prison-cell.html   # Hidden AR experience (QR code only)
```

## 🎯 Setting Up the AR Target Image

### Step 1: Create Your Target Image
1. Create a printable marker image (recommended: 300x300px to 1000x1000px)
2. Use high-contrast images with distinct features
3. Avoid solid colors or simple patterns
4. Save as PNG or JPG

### Step 2: Compile with mind-AR
You need to compile your target image into a `.mind` file:

**Option A: Use the Online Compiler**
1. Go to: https://hiukim.github.io/mind-ar-js-doc/tools/compile
2. Upload your marker image
3. Click "Start" to compile
4. Download the `.mind` file
5. Save it as `assets/targets/prison-cell-marker.mind`

**Option B: Use Node.js Compiler**
```bash
npm install -g mind-ar-js
mindar-image-compiler --input your-marker-image.png --output prison-cell-marker.mind
```

### Step 3: Print Your Marker
- Print the marker image on paper (A4 size recommended)
- Place it flat on the ground in the prison cell center
- Ensure good lighting for tracking

## 🚀 Testing Locally

### Prerequisites
- Install [Visual Studio Code](https://code.visualstudio.com/)
- Install Live Server extension for VS Code

### Steps:
1. Open the `lifeonmarzj-website` folder in VS Code
2. Right-click on `index.html` → "Open with Live Server"
3. Your website will open at `http://localhost:5500`

### Testing the AR Experience:
1. On mobile, go to: `http://YOUR-COMPUTER-IP:5500/ar-experiences/prison-cell.html`
2. Allow camera access
3. Point camera at printed marker
4. Prison cell should appear!

**Find your computer's IP:**
- Windows: `ipconfig` in Command Prompt (look for IPv4)
- Mac/Linux: `ifconfig` (look for inet)

## 🌍 Deploying to lifeonmarzj.com

### Recommended Hosting Options:

#### Option 1: Netlify (Easy, Free)
1. Create account at [Netlify](https://netlify.com)
2. Drag and drop your `lifeonmarzj-website` folder
3. Set custom domain: lifeonmarzj.com
4. Configure DNS at your domain registrar:
   - Add CNAME record pointing to Netlify

#### Option 2: GitHub Pages (Free)
1. Create GitHub account
2. Create repository named `lifeonmarzj-website`
3. Upload all files
4. Enable GitHub Pages in settings
5. Configure custom domain

#### Option 3: Vercel (Easy, Free)
1. Create account at [Vercel](https://vercel.com)
2. Import your project folder
3. Set custom domain
4. Deploy!

### Domain Configuration:
After choosing hosting, update your domain DNS settings at your registrar (where you bought lifeonmarzj.com):
- Point A record to hosting provider's IP
- Or add CNAME record to hosting provider's URL

## 🔒 Making AR Experience Hidden

### Creating the QR Code URL:
1. Your AR experience URL will be:
   ```
   https://lifeonmarzj.com/ar-experiences/prison-cell.html
   ```

2. Generate QR code:
   - Use: https://www.qr-code-generator.com/
   - Enter your AR URL
   - Download and print QR code

3. The AR page is hidden because:
   - Not linked from main website
   - Blocked in `robots.txt` (won't appear in Google)
   - Only accessible via direct URL (QR code)

## 📱 Visitor Experience:

1. Visitor scans QR code on their phone
2. Opens AR experience URL
3. Grants camera permission
4. Points phone at marker on ground
5. Prison cell appears in AR!
6. Can walk around and view from all angles

## 🎨 Customizing Your Website:

### Update Portfolio Content:
Edit `index.html`:
- Replace placeholder text with your content
- Add your projects to portfolio section
- Update about section with your bio

### Change Colors/Style:
Edit `css/style.css`:
- Modify color variables
- Adjust fonts, spacing, etc.

### Add Your 3D Models:
When you have your furniture models ready:

1. Place GLB/GLTF files in `assets/models/`

2. Edit `ar-experiences/prison-cell.html`:
   - In `<a-assets>`, uncomment and add:
     ```html
     <a-asset-item id="bed-model" src="../assets/models/bed.glb"></a-asset-item>
     ```

   - Replace placeholder boxes with:
     ```html
     <a-entity
         gltf-model="#bed-model"
         position="1.05 0.3 -1.45"
         scale="1 1 1">
     </a-entity>
     ```

## 🛠️ Technical Details:

### AR Prison Cell Measurements:
- Cell: 4m (length) x 2.6m (width) x 3m (height)
- Bed: 2m x 0.9m (right wall, near window)
- Toilet: 0.4m x 0.5m (left corner, near door)
- Table: 0.8m x 0.6m (left wall, centered)
- Chair: 0.4m x 0.4m (near table)

### Technologies Used:
- **A-Frame 1.4.2**: WebVR/AR framework
- **mind-AR 1.2.2**: Image tracking library
- **HTML5/CSS3/JavaScript**: Frontend
- **WebXR**: Browser AR capabilities

## 📞 Support:

If you need help:
1. Check browser console for errors (F12)
2. Ensure HTTPS is enabled (required for camera access)
3. Test on different devices
4. Verify marker image has good contrast

## 🎉 Next Steps:

1. ✅ Create and compile your target image
2. ✅ Test AR experience locally
3. ✅ Customize portfolio content
4. ✅ Choose hosting provider
5. ✅ Deploy website
6. ✅ Configure domain
7. ✅ Print QR codes and markers
8. ✅ Set up exhibition!

---

**Website:** https://lifeonmarzj.com
**AR Experience:** https://lifeonmarzj.com/ar-experiences/prison-cell.html

Good luck with your exhibition! 🎨🔒
