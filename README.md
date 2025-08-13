# 📋 Quick Report - Complete Full-Stack Application

A professional React-based documentation tool for creating image reports with sections, annotations, and export capabilities.

## 🚀 Quick Deploy Options

### Option 1: Vercel (Recommended)
```bash
npm install -g vercel
vercel --prod
```

### Option 2: Railway 
```bash
npm install -g @railway/cli
railway login
railway deploy
```

### Option 3: Render
- Upload to GitHub and connect to Render
- Uses included `render.yaml` configuration

### Option 4: Heroku
```bash
heroku create your-app-name
git push heroku main
```

### Option 5: Docker
```bash
docker build -t quick-report .
docker run -p 5000:5000 quick-report
```

## ✨ Features

- ✅ **Section Management** - Create, edit, delete, and organize sections
- ✅ **Image Upload** - Drag & drop multiple images with validation
- ✅ **Image Organization** - Reorder and edit image titles
- ✅ **Export Options** - Generate PNG images and PDF reports
- ✅ **Responsive Design** - Works on desktop, tablet, and mobile
- ✅ **Material Design** - Clean, professional interface
- ✅ **Real-time Updates** - Optimistic UI with instant feedback

## 🛠 Local Development

```bash
npm install
npm run dev
```

Visit: http://localhost:5000

## 📦 Production Build

```bash
npm run build
npm start
```

## 📁 Package Contents

- `dist/` - Production build files
- `client/` - React frontend source
- `server/` - Express.js backend source
- `shared/` - TypeScript schemas
- `deployment-configs/` - Platform-specific configurations
- `DEPLOYMENT_GUIDE.md` - Detailed deployment instructions

## 🔧 Tech Stack

- **Frontend:** React, TypeScript, Tailwind CSS, shadcn/ui
- **Backend:** Express.js, Multer (file uploads)
- **Build Tools:** Vite, esbuild
- **Export:** html2canvas, jsPDF
- **Styling:** Material Design principles

## 📞 Support

For deployment help, check `DEPLOYMENT_GUIDE.md` for platform-specific instructions and troubleshooting.