# 🚀 Free Deployment Guide for PneumoScan AI

This guide will help you deploy your Streamlit pneumonia classifier app for **FREE** on Streamlit Community Cloud.

## 📋 Prerequisites

1. **GitHub Account** - [Sign up here](https://github.com/signup) (Free)
2. **Streamlit Community Cloud Account** - [Sign up here](https://streamlit.io/cloud) (Free)
3. **Git installed** - [Download here](https://git-scm.com/downloads)

---

## 🎯 Option 1: Deploy to Streamlit Community Cloud (RECOMMENDED)

Streamlit Community Cloud is **100% FREE** and specifically designed for Streamlit apps!

### Step 1: Push Your Code to GitHub

1. **Initialize Git repository** (if not already done):
   ```bash
   cd "d:\joint\pnemonia classifier\pneumonia-classification-web-app-python-streamlit-main"
   git init
   git add .
   git commit -m "Initial commit - PneumoScan AI"
   ```

2. **Create a new repository on GitHub**:
   - Go to [github.com/new](https://github.com/new)
   - Name it: `pneumoscan-ai` (or any name you prefer)
   - Set it to **Public** (required for free Streamlit hosting)
   - **Do NOT** initialize with README (you already have one)
   - Click "Create repository"

3. **Push your code to GitHub**:
   ```bash
   git remote add origin https://github.com/YOUR_USERNAME/pneumoscan-ai.git
   git branch -M main
   git push -u origin main
   ```
   Replace `YOUR_USERNAME` with your actual GitHub username.

### Step 2: Deploy on Streamlit Community Cloud

1. **Go to** [share.streamlit.io](https://share.streamlit.io)

2. **Sign in** with your GitHub account

3. **Click "New app"**

4. **Fill in the details**:
   - **Repository**: Select `YOUR_USERNAME/pneumoscan-ai`
   - **Branch**: `main`
   - **Main file path**: `main.py`
   - **App URL** (optional): Choose a custom URL or use default

5. **Click "Deploy"**

6. **Wait for deployment** (usually 2-5 minutes)

7. **Your app is live!** 🎉
   - You'll get a URL like: `https://pneumoscan-ai.streamlit.app`
   - Share this URL with anyone!

### ⚙️ Advanced Settings (Optional)

If your app needs more resources, click "Advanced settings" before deploying:
- **Python version**: 3.11
- **Secrets**: Not needed for this app

### 🔄 Updating Your Deployed App

When you make changes:
```bash
git add .
git commit -m "Updated features"
git push
```
Streamlit will automatically redeploy your app!

---

## 🎯 Option 2: Deploy to Render (Alternative)

Render offers free hosting for web apps with some limitations.

### Step 1: Push to GitHub (same as above)

### Step 2: Deploy on Render

1. **Go to** [render.com](https://render.com) and sign up

2. **Click "New +" → "Web Service"**

3. **Connect your GitHub repository**

4. **Configure the service**:
   - **Name**: `pneumoscan-ai`
   - **Environment**: `Python 3`
   - **Build Command**: `pip install -r requirements.txt`
   - **Start Command**: `streamlit run main.py --server.port=$PORT --server.address=0.0.0.0`
   - **Instance Type**: `Free`

5. **Click "Create Web Service"**

6. **Wait for deployment** (5-10 minutes)

**Note**: Render free tier may spin down after inactivity and has limited resources.

---

## 🎯 Option 3: Deploy to Hugging Face Spaces

Great for ML apps with large models!

### Step 1: Create Hugging Face Account

1. Go to [huggingface.co/join](https://huggingface.co/join)
2. Sign up for free

### Step 2: Create a New Space

1. Click your profile → **"New Space"**
2. **Space name**: `pneumoscan-ai`
3. **License**: MIT
4. **Select SDK**: `Streamlit`
5. **Space hardware**: `CPU basic (Free)`
6. Click **"Create Space"**

### Step 3: Upload Your Files

You can either:

**Option A: Git Push** (Recommended)
```bash
git remote add huggingface https://huggingface.co/spaces/YOUR_USERNAME/pneumoscan-ai
git push huggingface main
```

**Option B: Web Upload**
- Click "Files" → "Add file" → "Upload files"
- Upload all your project files

### Step 4: Your App is Live!
- URL: `https://huggingface.co/spaces/YOUR_USERNAME/pneumoscan-ai`

---

## 📊 Comparison of Free Hosting Options

| Feature | Streamlit Cloud | Render | Hugging Face |
|---------|----------------|--------|--------------|
| **Setup Difficulty** | ⭐ Easy | ⭐⭐ Medium | ⭐⭐ Medium |
| **Deployment Speed** | 2-5 mins | 5-10 mins | 3-7 mins |
| **RAM** | 1 GB | 512 MB | 16 GB |
| **CPU** | 0.2 cores | 0.1 cores | 2 cores |
| **Always On** | ✅ Yes | ❌ Sleeps | ✅ Yes |
| **Custom Domain** | ❌ No | ✅ Yes | ❌ No |
| **Best For** | Streamlit apps | Any web app | ML/AI apps |

**RECOMMENDATION**: Use **Streamlit Community Cloud** - it's the easiest and most reliable for Streamlit apps!

---

## 🐛 Troubleshooting

### Issue: "Module not found" error
**Solution**: Make sure `requirements.txt` is in your repository root.

### Issue: App crashes on startup
**Solution**: Check if `model/pneumonia_classifier.h5` and `model/labels.txt` are uploaded.

### Issue: File too large for GitHub
**Solution**: If your model file (`.h5`) is >100MB:
1. Install Git LFS: `git lfs install`
2. Track the model: `git lfs track "*.h5"`
3. Commit and push again

### Issue: Image won't load
**Solution**: Make sure `bgs/bg5.jpg` exists in your repository.

---

## 📈 Monitoring Your App

### Streamlit Cloud
- View logs: [share.streamlit.io/YOUR_USERNAME/pneumoscan-ai](https://share.streamlit.io)
- See analytics: Click on your app → "Analytics"

### Check App Status
Visit your app URL to ensure it's running properly.

---

## 🔒 Security Notes

1. ⚠️ **Never commit sensitive data** (API keys, passwords)
2. ✅ The `.gitignore` file is configured to exclude sensitive files
3. ✅ This app doesn't require any API keys or secrets

---

## 💡 Tips for Success

1. **Test Locally First**: Run `streamlit run main.py` to ensure it works
2. **Keep Model File Small**: Compress if possible (current size is fine)
3. **Use Public Repository**: Required for free Streamlit Cloud hosting
4. **Monitor Usage**: Check Streamlit analytics to see how many people use your app

---

## 🎓 Next Steps After Deployment

1. **Share your app URL** with classmates, professors, or portfolio
2. **Add custom domain** (on Render) for professional look
3. **Enable Google Analytics** to track visitors
4. **Add to your resume/portfolio** - you've built a deployed ML app!

---

## 📞 Need Help?

- **Streamlit Docs**: [docs.streamlit.io](https://docs.streamlit.io)
- **Streamlit Forum**: [discuss.streamlit.io](https://discuss.streamlit.io)
- **GitHub Issues**: Create an issue in your repository

---

## ✅ Deployment Checklist

Before deploying, ensure:

- [ ] All files are in the repository
- [ ] `requirements.txt` is present and correct
- [ ] `main.py` runs locally without errors
- [ ] Model file (`.h5`) and labels are included
- [ ] Background image exists in `bgs/` folder
- [ ] `.gitignore` excludes unnecessary files
- [ ] Repository is pushed to GitHub
- [ ] Repository is **Public** (for free hosting)

---

**Good luck with your deployment! 🚀**

Your PneumoScan AI app will be accessible worldwide once deployed!
