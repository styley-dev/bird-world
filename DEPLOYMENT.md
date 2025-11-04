# How to Host Bird World on a Website

Since this is a static HTML game, you have many free hosting options! Here are the easiest methods:

## Option 1: GitHub Pages (FREE - Recommended) ⭐

### Steps:

1. **Create a GitHub account** (if you don't have one):
   - Go to https://github.com
   - Sign up for a free account

2. **Create a new repository**:
   - Click the "+" icon in the top right
   - Select "New repository"
   - Name it (e.g., "bird-world-game")
   - Make it **Public**
   - Click "Create repository"

3. **Upload your files**:
   - Click "uploading an existing file"
   - Drag and drop `index.html` and `README.md` into the repository
   - Click "Commit changes"

4. **Enable GitHub Pages**:
   - Go to **Settings** tab in your repository
   - Scroll down to **Pages** section (in left sidebar)
   - Under "Source", select **main branch** (or master)
   - Click **Save**
   - Wait a minute, then your site will be live at:
     `https://your-username.github.io/bird-world-game/`

**That's it!** Your game is now live on the internet! 🎉

---

## Option 2: Netlify (FREE - Drag & Drop)

### Steps:

1. Go to https://www.netlify.com
2. Sign up for a free account (can use GitHub to sign in)
3. On the dashboard, find the **"Sites"** section
4. Drag and drop your entire `Bird World` folder onto the drop zone
5. Your site will be deployed instantly!
6. You'll get a URL like: `https://random-name-123456.netlify.app`
7. You can customize the URL in Site settings → Domain settings

**Pros**: Instant deployment, automatic HTTPS, custom domains

---

## Option 3: Vercel (FREE)

### Steps:

1. Go to https://vercel.com
2. Sign up (can use GitHub)
3. Click "Add New..." → "Project"
4. Import your GitHub repository, OR
5. Drag and drop your folder
6. Deploy!

---

## Option 4: Surge.sh (FREE - Command Line)

### Steps:

1. Install Node.js if you don't have it: https://nodejs.org
2. Open terminal/command prompt
3. Install Surge: `npm install -g surge`
4. Navigate to your project folder:
   ```bash
   cd "c:\Users\lpatterson\Desktop\Bird World"
   ```
5. Run: `surge`
6. Follow the prompts to create account and deploy
7. Your site will be live at: `your-site-name.surge.sh`

---

## Option 5: Traditional Web Hosting

If you already have web hosting (like cPanel, GoDaddy, etc.):

1. **Via FTP/SFTP**:
   - Connect to your hosting using FileZilla or similar
   - Upload `index.html` to the `public_html` or `www` folder
   - Access at: `https://yourdomain.com/index.html`
   - Or rename to `index.html` and it will load automatically

2. **Via File Manager**:
   - Log into your hosting control panel
   - Open File Manager
   - Navigate to public_html/www folder
   - Upload `index.html`
   - Done!

---

## Making it More Professional

### Custom Domain (Optional):

- **Netlify/Vercel**: Go to domain settings, add your custom domain
- **GitHub Pages**: In repo Settings → Pages, add custom domain
- You'll need to configure DNS settings with your domain registrar

### Custom URL Path:

If you want the game at `yourdomain.com/game` instead of `yourdomain.com/index.html`:
- Create a folder called `game`
- Put `index.html` inside it
- Access at `yourdomain.com/game/`

---

## Quick Test Before Uploading

Before uploading, test locally:
1. Double-click `index.html` - it should open in your browser
2. Test all controls and features
3. If everything works, you're ready to deploy!

---

## Recommended: GitHub Pages

GitHub Pages is the **easiest and most reliable** free option because:
- ✅ Free forever
- ✅ Easy updates (just push new code)
- ✅ Reliable uptime
- ✅ Free HTTPS/SSL
- ✅ Can use custom domain
- ✅ No file size limits for reasonable games

---

## Need Help?

- **GitHub Pages**: https://docs.github.com/en/pages
- **Netlify**: https://docs.netlify.com
- **Vercel**: https://vercel.com/docs

Your game is ready to share with the world! 🌍🐦
