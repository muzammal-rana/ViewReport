# Quick Report - Full-Stack Deployment Guide

This package contains everything needed to deploy the complete Quick Image Report application with all features working.

## 🚀 Platform-Specific Deployment Instructions

### 1. Vercel (Recommended - Easy Setup)
```bash
npm install -g vercel
vercel --prod
```
- Supports serverless functions
- Automatic scaling
- Free tier: 100GB bandwidth/month

### 2. Railway (Great for Node.js)
```bash
npm install -g @railway/cli
railway login
railway deploy
```
- Built-in PostgreSQL
- Free tier: 512MB RAM, 1GB disk
- Automatic deployments from Git

### 3. Render (Free Tier with Database)
- Upload this package to GitHub
- Connect repository to Render
- Uses `render.yaml` configuration
- Free tier: 512MB RAM, PostgreSQL included

### 4. Heroku (Classic Platform)
```bash
npm install -g heroku
heroku create your-app-name
git push heroku main
```
- Uses `Procfile` and `app.json`
- Eco dyno: $5/month
- PostgreSQL add-on available

### 5. Docker (Any Platform)
```bash
docker build -t quick-report .
docker run -p 5000:5000 quick-report
```
- Uses `Dockerfile` and `.dockerignore`
- Deploy to AWS, GCP, Azure, DigitalOcean

## 📦 What's Included

### Core Application
- `dist/` - Production build (optimized)
- `client/` - React frontend source
- `server/` - Express.js backend source
- `shared/` - TypeScript schemas

### Configuration Files
- `vercel.json` - Vercel serverless configuration
- `render.yaml` - Render platform configuration
- `railway.json` - Railway deployment settings
- `Dockerfile` - Docker containerization
- `Procfile` - Heroku process definition
- `app.json` - Heroku app configuration

### Features Available
✅ Create and manage report sections
✅ Upload and organize images (drag & drop)
✅ Edit image titles and descriptions
✅ Export reports as PNG images
✅ Export reports as PDF files
✅ Responsive Material Design interface
✅ In-memory data storage (upgradeable to database)

## 🛠 Local Development
```bash
npm install
npm run dev
```
Access at: http://localhost:5000

## 🏗 Production Build
```bash
npm run build
npm start
```

## 🔧 Environment Variables (Optional)
- `NODE_ENV=production` (automatically set by platforms)
- `PORT` (automatically set by hosting platforms)

## 📊 Resource Requirements
- **RAM:** 512MB minimum
- **Storage:** 1GB for images
- **Node.js:** Version 18+ required

## 🆘 Troubleshooting

### Common Issues:
1. **Build Fails:** Ensure Node.js 18+ is available
2. **Images Not Uploading:** Check file permissions on uploads folder
3. **API Errors:** Verify all routes are accessible

### Platform-Specific Notes:
- **Vercel:** Serverless functions have 50MB deployment limit
- **Railway:** Persistent storage included by default
- **Render:** Free tier has 750 hours/month limit
- **Heroku:** Eco dynos sleep after 30 minutes of inactivity

## 📚 Tech Stack
- Frontend: React, TypeScript, Tailwind CSS, shadcn/ui
- Backend: Express.js, Multer (file uploads)
- Build: Vite, esbuild
- Export: html2canvas, jsPDF