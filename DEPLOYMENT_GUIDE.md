# 🚀 GitHub & Vercel Deployment Guide for Lucy Gray R Portfolio

## Step-by-Step Setup (5-10 minutes)

### STEP 1: Prepare Your GitHub Account

1. Go to [github.com](https://github.com)
2. Sign up (if you don't have an account) or log in
3. Remember your username (you'll need it)

---

### STEP 2: Create a New GitHub Repository

1. Click the **+** icon in top-right corner
2. Select **"New repository"**
3. Fill in:
   - **Repository name:** `lucygrayr-portfolio`
   - **Description:** "Lucy Gray R - Creative AI Studio Portfolio"
   - **Public** (so anyone can see it)
   - ✅ Check "Add a README file"
   - ✅ Check "Add .gitignore" (select Node)
4. Click **"Create repository"**

---

### STEP 3: Upload Files to GitHub

#### Option A: Using Git Command Line (Recommended)

1. **Open Terminal/Command Prompt** on your computer
2. Navigate to your project folder:

   ```bash
   cd path/to/lucygrayr-portfolio
   ```

3. **Initialize Git:**

   ```bash
   git init
   git add .
   git commit -m "Initial commit: Lucy Gray R portfolio website"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/lucygrayr-portfolio.git
   git push -u origin main
   ```

   Replace `YOUR_USERNAME` with your actual GitHub username.

4. **You'll see:**

   ```text
   Enumerating objects: X done.
   Counting objects: 100% (X/X) done.
   Writing objects: 100% (X/X) done.
   Total X (delta X), reused 0 (delta 0)
   ...
   To github.com:YOUR_USERNAME/lucygrayr-portfolio.git
    * [new branch]      main -> main
   ```

#### Option B: Using GitHub Web Interface

1. Go to your new repository on GitHub
2. Click **"Add file"** → **"Upload files"**
3. Drag and drop all files from the `lucygrayr-portfolio` folder
4. Click **"Commit changes"**

---

### STEP 4: Deploy to Vercel

1. Go to [vercel.com](https://vercel.com)
2. Click **"Sign Up"** (or log in if you have an account)
3. Choose **"Continue with GitHub"**
4. Authorize Vercel to access your GitHub
5. You'll see a list of your repositories
6. Find **`lucygrayr-portfolio`** and click **"Import"**
7. Click **"Deploy"** (Vercel auto-detects it's a static site)
8. Wait 30-60 seconds for deployment ⏳
9. You'll see a success screen with your live URL!

**Your site is now live!** 🎉

The URL will be: `https://lucygrayr-portfolio.vercel.app` (or custom domain)

---

### STEP 5: Set Up Contact Form (Optional but Recommended)

#### Using Formspree (Easiest)

1. Go to [formspree.io](https://formspree.io)
2. Sign up with email
3. Click **"New Form"**
4. Name it `lucygrayr-contact`
5. Copy your Form ID (looks like `f_xxxxx`)
6. In your `index.html`, find this line (around line 680):

   ```javascript
   const response = await fetch('https://formspree.io/f/YOUR_FORM_ID', {
   ```

7. Replace `YOUR_FORM_ID` with your actual Form ID
8. Git commit and push the change:

   ```bash
   git add index.html
   git commit -m "Add Formspree form ID"
   git push
   ```

9. Vercel auto-redeployss! Test the form.

---

## 🎯 What You Can Do Now

✅ Visit your live site: `https://lucygrayr-portfolio.vercel.app`  
✅ Share it on Instagram, Twitter, LinkedIn, email  
✅ Make changes in VS Code and push to GitHub  
✅ Vercel auto-deploys every time you push  
✅ Contact form receives submissions  
✅ Mobile-responsive on all devices  

---

## 📝 Making Updates (After Deployment)

### Change Content

1. Open `index.html` in VS Code
2. Edit text, colors, or add new projects
3. Save the file
4. Open Terminal and run:

   ```bash
   git add .
   git commit -m "Update portfolio content"
   git push
   ```

5. Vercel auto-redeploys in ~30 seconds!
6. Refresh your live site to see changes

### Change Colors

Look for this section in `index.html`:

```css
:root {
  --bg: #0a0a0a;        /* Dark background */
  --accent: #d8b36a;    /* Gold color */
  --accent-2: #6f0f1f;  /* Dark red */
}
```

Change hex colors and push! ✨

---

## 🔧 Using VS Code

### Setup (First Time)

1. Install [VS Code](https://code.visualstudio.com)
2. Install **Git** from [git-scm.com](https://git-scm.com)
3. Open the `lucygrayr-portfolio` folder in VS Code
4. Install "Live Server" extension:
   - Click Extensions (Ctrl+Shift+X)
   - Search "Live Server"
   - Install by Ritwick Dey
5. Right-click `index.html` → **"Open with Live Server"**

### Every Time You Code

1. Make changes in VS Code
2. Live Server auto-refreshes your browser
3. When happy, run:

   ```bash
   git add .
   git commit -m "Your message"
   git push
   ```

---

## ❌ Troubleshooting

### "git command not found"

→ Install Git from [git-scm.com](https://git-scm.com)

### "fatal: remote origin already exists"

→ Run: `git remote remove origin` then try again

### "Changes not showing on Vercel"

→ Wait 30-60 seconds and refresh. Check the Vercel deployments tab.

### Contact form not working

→ Make sure Formspree Form ID is correct and you've set up the form

### Can't push to GitHub

→ Check you have write access to the repo. Try: `git config --global user.email "your@email.com"`

---

## 📊 Next Steps

### Add Real Images

```bash
mkdir public
# Add your project images to public/ folder
# Update src="" in HTML to point to public/image.jpg
```

### Add Custom Domain

1. Buy domain (Namecheap, GoDaddy, etc.)
2. In Vercel: Settings → Domains
3. Add your domain
4. Update DNS records (Vercel will guide you)

### Analytics

Add to `<head>` in HTML:

```html
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

---

## 🎬 Mnemonics (Remember This!)

**GitHub** = Where your code lives (backup + version control)  
**Vercel** = Where your website is published (hosting)  
**Push** = Upload changes from your computer to GitHub  
**Deploy** = Vercel auto-publishes when you push  
**Commit** = Save a version with a description  

---

## 💬 Need Help?

- **Git Issues:** [GitHub Docs](https://docs.github.com)
- **Vercel Issues:** [Vercel Support](https://vercel.com/support)
- **Code Questions:** [VS Code Docs](https://code.visualstudio.com/docs)

---

**You're all set! 🚀 Your portfolio is production-ready.**

Questions? Check the README.md in your project folder.
