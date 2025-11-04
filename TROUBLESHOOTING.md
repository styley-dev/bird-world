# GitHub Pages Troubleshooting Guide

If your GitHub Pages URL won't load, try these steps in order:

## Step 1: Check the Basics

### ✅ Is your repository Public?
- GitHub Pages FREE only works with **Public** repositories
- Go to your repo → Settings → scroll down to "Danger Zone"
- If it says "Change visibility", your repo is private
- Click it and make it Public

### ✅ Is the file named `index.html`?
- The file MUST be named exactly `index.html` (lowercase)
- Not `Index.html`, `INDEX.HTML`, or any variation
- Check in your repository that the file shows as `index.html`

### ✅ Is it in the root folder?
- `index.html` should be in the **root** of your repository
- NOT inside a subfolder
- The URL structure should be: `your-repo/index.html` (in the root)

## Step 2: Check GitHub Pages Settings

1. Go to your repository on GitHub
2. Click **Settings** tab
3. Scroll down to **Pages** (in left sidebar)
4. Check:
   - **Source**: Should be set to "Deploy from a branch"
   - **Branch**: Should be `main` (or `master` if older repo)
   - **Folder**: Should be `/ (root)`
5. Click **Save**
6. Wait 1-2 minutes

## Step 3: Check Your URL Format

Your URL should be exactly:
```
https://YOUR-USERNAME.github.io/REPOSITORY-NAME/
```

Common mistakes:
- ❌ `https://github.com/username/repo` (this is the repo page, not the site)
- ❌ Missing `.github.io` in the URL
- ✅ `https://username.github.io/bird-world-game/` (correct format)

## Step 4: Wait for Deployment

- First deployment can take **1-5 minutes**
- After saving Pages settings, you'll see a message like "Your site is ready to be published"
- Check the Actions tab (if enabled) to see deployment status
- Once deployed, the Pages settings will show a green checkmark

## Step 5: Hard Refresh Your Browser

Sometimes browsers cache the old "404" page:
- **Windows/Linux**: Press `Ctrl + F5` or `Ctrl + Shift + R`
- **Mac**: Press `Cmd + Shift + R`
- Or open in an incognito/private window

## Step 6: Check for Build Errors

1. Go to **Settings** → **Pages**
2. Look for any error messages (usually in red)
3. Check the **Actions** tab for deployment logs
4. Common errors:
   - File not found (wrong location)
   - Build failed (less likely with static HTML)
   - Jekyll build error (can happen if GitHub tries to process the HTML)

## Step 7: Disable Jekyll (If Needed)

GitHub sometimes tries to process HTML files with Jekyll. To disable:

1. In your repository root, create a file named `.nojekyll` (no extension, starts with a dot)
2. This file can be empty
3. Commit and push it
4. Wait for redeployment

## Step 8: Verify File Contents

1. Click on `index.html` in your repository
2. Click "Raw" button
3. Check if the file shows properly (should see HTML code)
4. If file looks corrupted or incomplete, re-upload it

## Step 9: Check Repository Structure

Your repository should look like this:
```
bird-world-game/
  ├── index.html
  ├── README.md (optional)
  └── .nojekyll (optional, if needed)
```

NOT like this:
```
bird-world-game/
  └── Bird World/
      └── index.html  ❌ (wrong - file is in subfolder)
```

## Quick Fix Checklist

Before asking for more help, verify:
- [ ] Repository is **Public**
- [ ] File is named `index.html` (exact spelling)
- [ ] File is in the **root** folder (not in a subfolder)
- [ ] GitHub Pages is enabled in Settings → Pages
- [ ] Source branch is set to `main` or `master`
- [ ] You're using the correct URL: `username.github.io/repo-name/`
- [ ] You waited at least 2 minutes after enabling Pages
- [ ] You tried a hard refresh (Ctrl+F5)

## Still Not Working?

If all the above are correct but it still doesn't work:

1. **Try accessing the file directly**:
   ```
   https://YOUR-USERNAME.github.io/REPO-NAME/index.html
   ```
   (Add `/index.html` at the end)

2. **Check the exact repository name**:
   - Repository name might have spaces or special characters
   - GitHub converts spaces to hyphens in URLs
   - Example: "Bird World" becomes "Bird-World" in URL

3. **Create a test file**:
   - Create a simple file named `test.html` with just `<h1>Hello</h1>`
   - Upload it to root
   - Try: `https://username.github.io/repo-name/test.html`
   - If this works but index.html doesn't, there's an issue with index.html

## Getting Your Exact URL

To find your exact GitHub Pages URL:
1. Go to your repository
2. Click **Settings** → **Pages**
3. At the top it will show: "Your site is live at: [URL]"
4. Copy that exact URL

## Common Error Messages

**"404 File not found"**
- File is in wrong location
- File name is wrong
- Repository structure issue

**"Site not found"**
- Repository is private (must be public for free Pages)
- Pages not enabled
- Wrong URL

**"Page build failed"**
- Usually means Jekyll error
- Add `.nojekyll` file to root

---

Still having issues? Double-check all the steps above and let me know what specific error message you see!
