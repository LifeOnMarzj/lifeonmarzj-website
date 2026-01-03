# Quick Start Guide

## 🚀 Get Started in 5 Minutes!

### 1. Open in Visual Studio Code
```bash
cd C:\Users\home\Documents\lifeonmarzj-website
code .
```

### 2. Install Live Server Extension
1. In VS Code, press `Ctrl+Shift+X`
2. Search for "Live Server"
3. Click "Install" on the extension by Ritwick Dey

### 3. Start Local Server
1. Right-click on `index.html`
2. Select "Open with Live Server"
3. Your browser will open automatically!

### 4. Test AR Experience on Phone
1. Find your computer's IP address:
   - Windows: Open Command Prompt, type `ipconfig`
   - Look for "IPv4 Address" (e.g., 192.168.1.100)

2. On your phone's browser, go to:
   ```
   http://YOUR-IP-ADDRESS:5500/ar-experiences/prison-cell.html
   ```
   Example: `http://192.168.1.100:5500/ar-experiences/prison-cell.html`

3. **IMPORTANT**: You need to create the target marker first!

---

## 📸 Creating Your AR Marker (MUST DO FIRST!)

### Step 1: Create Marker Image
Create a simple image (or use your logo/design):
- Size: 500x500px or larger
- High contrast (black/white patterns work well)
- Avoid plain colors
- Save as PNG

### Step 2: Compile to .mind File
**Easiest method - Use Online Tool:**

1. Go to: https://hiukim.github.io/mind-ar-js-doc/tools/compile
2. Click "Choose File" and upload your marker image
3. Click "Start"
4. Wait for compilation (takes 1-2 minutes)
5. Click "Download Compiled" button
6. Save the downloaded file

### Step 3: Add to Project
1. Create folder: `assets/targets/`
2. Rename downloaded file to: `prison-cell-marker.mind`
3. Place it in: `assets/targets/prison-cell-marker.mind`

### Step 4: Print the Marker
1. Print your original marker image (A4 size)
2. Place it flat on the ground where you want the AR experience

---

## 🌐 Deploy to Internet

### Recommended: Use Netlify (Easiest!)

1. **Sign up**: Go to https://netlify.com and create free account

2. **Deploy**:
   - Click "Add new site" → "Deploy manually"
   - Drag and drop your `lifeonmarzj-website` folder
   - Wait 30 seconds - Done! You get a URL like `random-name-123.netlify.app`

3. **Add Custom Domain** (lifeonmarzj.com):
   - In Netlify dashboard, click "Domain settings"
   - Click "Add custom domain"
   - Enter: `lifeonmarzj.com`
   - Follow DNS instructions provided
   - Go to your domain registrar and update DNS settings
   - Wait 24-48 hours for DNS propagation

4. **Enable HTTPS**:
   - Netlify enables this automatically
   - Required for camera access in AR!

---

## 🔗 Creating Your QR Code

Once deployed, your AR URL will be:
```
https://lifeonmarzj.com/ar-experiences/prison-cell.html
```

**Generate QR Code:**
1. Go to: https://www.qr-code-generator.com/
2. Select "URL"
3. Enter your AR experience URL
4. Customize design if desired
5. Download QR code
6. Print and place in your exhibition!

---

## ✅ Checklist

- [ ] Open project in VS Code
- [ ] Install Live Server extension
- [ ] Create marker image (500x500px PNG)
- [ ] Compile marker at https://hiukim.github.io/mind-ar-js-doc/tools/compile
- [ ] Save as `assets/targets/prison-cell-marker.mind`
- [ ] Test locally with Live Server
- [ ] Test AR on phone using local IP
- [ ] Customize portfolio content in `index.html`
- [ ] Deploy to Netlify
- [ ] Configure domain (lifeonmarzj.com)
- [ ] Generate QR code
- [ ] Print QR code and marker
- [ ] Set up exhibition!

---

## 🆘 Common Issues

**AR not loading?**
- Make sure `prison-cell-marker.mind` file exists
- Check browser console (F12) for errors
- Ensure HTTPS is enabled (required for camera)

**Marker not tracking?**
- Ensure good lighting
- Keep marker flat and visible
- Don't use reflective surfaces
- Marker should be at least 10cm x 10cm when printed

**Can't access on phone?**
- Make sure phone and computer are on same WiFi
- Check firewall isn't blocking port 5500
- Try using computer's IP address instead of localhost

---

**Need Help?** Check the full README.md for detailed instructions!
