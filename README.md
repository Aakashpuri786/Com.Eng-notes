# 🎓 Computer Engineering Notes

> **A modern, student-friendly platform for exploring, previewing, and downloading NEB-aligned computer engineering study material for Class 11 and 12.**

![Website](https://img.shields.io/badge/Website-Live-brightgreen?style=flat-square&logo=vercel)
![License](https://img.shields.io/badge/License-Open%20Source-blue?style=flat-square)
![Vue](https://img.shields.io/badge/Vue-3.5-4FC08D?style=flat-square&logo=vue.js)
![Status](https://img.shields.io/badge/Status-Active-success?style=flat-square)

---

## 📱 Overview

**Computer Engineering Notes** is an interactive web application designed to centralize and organize engineering study material for high school students. The platform provides a seamless experience for browsing files, previewing content before download, and managing offline access to course material.

**Live Demo:** [https://com-eng-notes.vercel.app](https://com-eng-notes.vercel.app)

### Why This Project?

Students often struggle with:
- Fragmented study material scattered across multiple sources
- Downloading files without knowing their content
- Organizing offline material efficiently
- Navigating NEB-curriculum aligned resources

This platform solves these problems with a **clean interface**, **built-in preview capability**, and **structured organization**.

---

## ✨ Key Features

### 🎯 **Smart File Explorer**
- Browse GitHub-hosted notes repository with a modern, intuitive grid interface
- Folder-based organization matching subject structure
- Real-time search and filtering across all files
- Breadcrumb navigation for easy path tracking
- One-click folder open to navigate deep directory structures

### 👁️ **Preview Before Download**
- View **Markdown** notes with formatted rendering
- Display **images** (JPG, PNG, GIF, WebP, SVG) inline
- Preview **text and code files** with proper formatting
- Embed **PDFs and Office documents** using Google Docs Viewer
- Preview **HTML files** in an isolated iframe for security

### 📥 **Flexible Download Options**
- Download individual files directly to your device
- **Batch download entire folders as ZIP archives**
- Confirmation dialogs to prevent accidental downloads
- Status notifications with auto-hide feedback
- Rate-limit aware handling with error messages

### 🎨 **Beautiful, Responsive Design**
- **Dark theme** with modern glassmorphism effects
- Gradient accents (cyan, indigo, blue) for visual appeal
- **Mobile-first responsive layout** - works perfectly on all devices
- Smooth animations and transitions throughout
- Accessibility-focused design with semantic HTML

### 📚 **Subject-Organized Content**
The platform supports four key subjects:
- **Computer Organization & Architecture (COA)** - Hardware fundamentals and system design
- **Operating Systems (OS)** - Process management and resource allocation
- **Java Programming** - OOP principles and practical coding
- **Web & Mobile Applications** - Modern development and app design

### 🔍 **NEB Curriculum Aligned**
Content structured specifically for Nepal's National Examination Board (NEB) Computer Engineering syllabus for Class 11 and 12.

### ❓ **Built-in FAQ Section**
Quick answers to common questions about using the platform and accessing material.

---

## 🛠️ Technology Stack

### **Frontend Framework**
- **Vue 3** (v3.5.35) - Progressive JavaScript framework for interactive UIs
- **Vite** (v8.0.16) - Lightning-fast build tool and dev server
- **Tailwind CSS** (v4.3) - Utility-first CSS framework with @tailwindcss/vite plugin

### **Key Libraries**
| Library | Version | Purpose |
|---------|---------|---------|
| **JSZip** | ^3.10.1 | Create ZIP archives for folder downloads |
| **File-Saver** | ^2.0.5 | Browser file download API wrapper |
| **Marked** | ^18.0.4 | Parse and render Markdown content |
| **DOMPurify** | ^3.4.7 | Sanitize HTML to prevent XSS attacks |

### **Development Tools**
- **@vitejs/plugin-vue** (^6.0.7) - Vue 3 SFC support in Vite
- **Nodemon** (^3.1.10) - Auto-reload development server
- **Node.js** (v18+) - Runtime environment

### **Hosting & Deployment**
- **GitHub API** - Direct content delivery from GitHub repository
- **Vercel** - Fast, optimized deployment platform
- **Google Fonts** - Inter and Playfair Display typefaces

---

## 🚀 Getting Started

### Prerequisites
- **Node.js** (v18 or higher)
- **npm** or **yarn** package manager
- Git for cloning the repository

### Installation

1. **Clone the repository:**
```bash
git clone https://github.com/aakashpuree/Com.Eng-notes.git
cd Com.Eng-notes
```

2. **Install dependencies:**
```bash
npm install
```

3. **Start the development server:**
```bash
npm run dev
```

The application will be available at `http://localhost:5173` (or the port shown in your terminal).

### Available Scripts

```bash
# Development server with hot reload
npm run dev

# Development with file watching and auto-restart
npm run dev:watch

# Production build (generates optimized dist/ folder)
npm run build

# Preview production build locally
npm run preview
```

---

## 📁 Project Structure

```
Com.Eng-notes/
├── src/
│   ├── App.vue              # Root component (deprecated, kept for reference)
│   ├── ComEng.vue           # Main application component
│   ├── main.js              # Vue app initialization
│   └── style.css            # Global styles
├── index.html               # HTML entry point
├── vite.config.js           # Vite configuration
├── package.json             # Dependencies and scripts
├── styles.css               # Legacy stylesheet
├── script.js                # Legacy JavaScript (deprecated)
├── .gitignore               # Git ignore rules
└── README.md                # This file
```

### **Component Architecture**

**ComEng.vue** (Main Component)
- Handles all state management and logic
- Renders hero section with feature highlights
- Displays subject cards with descriptions
- Manages the file explorer interface
- Controls preview modal and confirm dialogs
- Implements search and navigation

---

## 🎨 Design Highlights

### **Color Palette**
- **Primary Dark:** `#0f172a` (Slate 950) - Main background
- **Accent Cyan:** `#22d3ee` (Cyan 400) - Primary interactive elements
- **Secondary Blue:** `#3b82f6` (Blue 500) - Gradients and highlights
- **Light Text:** `#f1f5f9` (Slate 100) - High contrast readability

### **Typography**
- **Display Font:** Playfair Display (headings) - Elegant, modern look
- **Body Font:** Inter (default) - Clean, readable sans-serif
- Loaded from Google Fonts for consistency across devices

### **Visual Effects**
- **Glassmorphism** - Frosted glass effect with backdrop blur
- **Gradient Icons** - Colorful gradients for file type indicators
- **Smooth Transitions** - 200-300ms easing for all animations
- **Shadow Depth** - Layered shadows for visual hierarchy
- **Hover States** - Interactive feedback on all clickable elements

### **Responsive Breakpoints**
- **Mobile:** 0-640px (single column, full-width elements)
- **Tablet:** 641-1024px (2-column grid, adjusted spacing)
- **Desktop:** 1025px+ (3-4 column grid, full feature set)

---

## 🔧 Configuration

### **GitHub API Configuration**
The application connects to the GitHub repository defined in `src/ComEng.vue`:

```javascript
const REPO_OWNER = 'aakashpuree';
const REPO_NAME = 'class-11-notes';
const API_BASE = `https://api.github.com/repos/${REPO_OWNER}/${REPO_NAME}/contents/`;
```

**To use your own notes repository:**
1. Fork or create your own notes repository on GitHub
2. Update `REPO_OWNER` and `REPO_NAME` in `src/ComEng.vue`
3. Rebuild and redeploy

### **Environment Variables**
No environment variables are required for basic functionality. The app uses public GitHub API (subject to rate limits).

---

## 📊 Features Breakdown

### **File Preview Support**
| File Type | Support | Preview Method |
|-----------|---------|-----------------|
| Images (JPG, PNG, GIF, WebP, SVG) | ✅ | Direct image display |
| Markdown (.md) | ✅ | Rendered HTML with DOMPurify |
| Plain Text (.txt) | ✅ | Code block display |
| Code (JS, CSS, JSON, HTML) | ✅ | Pre-formatted text |
| PDF | ✅ | Google Docs Viewer iframe |
| Office (Doc, Docx, PPT, Excel) | ✅ | Google Docs Viewer iframe |
| Other files | ✅ | Raw text preview |

### **Navigation Features**
- **Breadcrumb Navigation** - Click any path segment to jump directly
- **Search Bar** - Real-time filtering of current folder contents
- **Back Button** - Return to previous folder with history tracking
- **Refresh** - Reload current folder from GitHub API
- **Keyboard Support** - Search input focus with standard shortcuts

---

## 🔒 Security & Performance

### **Security Measures**
- **DOMPurify Integration** - Sanitizes rendered HTML to prevent XSS attacks
- **Sandbox iframes** - Office documents loaded in isolated iframes
- **No Backend Required** - Direct GitHub API calls (no data processing server)
- **HTTPS Only** - All external resources loaded over secure connections

### **Performance Optimizations**
- **Lazy Loading** - Components load only when needed
- **CSS Animations** - Hardware-accelerated transforms for smooth 60fps
- **Efficient Search** - Real-time filtering without API calls
- **Responsive Images** - Properly sized images for different screen sizes
- **Minified Build** - Vite produces optimized production bundles

### **GitHub API Rate Limits**
- Public requests: 60 requests/hour (no authentication)
- Authenticated requests: 5,000 requests/hour (with token)
- Large folder downloads may trigger rate limits temporarily

---

## 🌐 Deployment

### **Deploy to Vercel** (Recommended)
```bash
# Using Vercel CLI
npm i -g vercel
vercel
```

### **Manual Deployment**
```bash
# Build production version
npm run build

# Deploy the 'dist' folder to your hosting service
```

### **Environment-Specific Configuration**
The app automatically detects the deployment environment and adjusts:
- Asset paths are relative for both local and production builds
- GitHub API calls work from any origin

---

## 📈 Usage Statistics

- **Total Subjects:** 4
- **Supported File Formats:** 15+
- **UI Components:** 20+ reusable Vue components
- **Lines of Code:** ~2,000+ (Vue, CSS, JavaScript combined)
- **Bundle Size:** ~180KB (gzipped, production build)

---

## 🐛 Known Limitations

1. **GitHub API Rate Limit** - Public requests limited to 60/hour
2. **Large Repository** - Very large folders may take time to load
3. **Network Dependent** - Requires internet connection to access notes
4. **Browser Compatibility** - Modern browsers (Chrome, Firefox, Safari, Edge) required
5. **PDF Preview** - Complex PDFs may not preview perfectly via Google Docs

### **Workarounds**
- Use GitHub API authentication token to increase rate limits
- Store frequently accessed files locally
- Use offline mode for already-downloaded material

---

## 🤝 Contributing

Contributions are welcome! To contribute:

1. **Fork the repository**
2. **Create a feature branch:** `git checkout -b feature/amazing-feature`
3. **Commit changes:** `git commit -m 'Add amazing feature'`
4. **Push to branch:** `git push origin feature/amazing-feature`
5. **Open a Pull Request**

### **Areas for Contribution**
- Adding new file preview types
- Improving mobile responsiveness
- Translating content to other languages
- Adding dark/light theme toggle
- Performance optimizations
- Documentation improvements
- UI/UX enhancements

---

## 📝 License

This project is **open source** and available for educational use. Feel free to fork, modify, and deploy for your own study material.

---

## 👨‍💻 Author

**Aakash Puri**
- GitHub: [@aakashpuree](https://github.com/aakashpuree)
- Website: [com-eng-notes.vercel.app](https://com-eng-notes.vercel.app)

---

## 🙏 Acknowledgments

- **Vue.js Community** - For the excellent framework and ecosystem
- **Tailwind CSS** - For utility-first CSS approach
- **Vercel** - For fast, reliable hosting
- **Students** - For feedback and feature requests
- **Contributors** - For improvements and bug fixes

---

## ❓ FAQ

### **How do I use this for my own notes?**
1. Create a GitHub repository with your notes organized in folders
2. Update `REPO_OWNER` and `REPO_NAME` in `src/ComEng.vue`
3. Deploy to Vercel or your preferred hosting

### **Can I download all notes at once?**
Select a top-level folder and click "Download" to get a ZIP archive of all contents.

### **Do I need an API key?**
No API key is required for public repositories. Public GitHub API allows 60 requests/hour.

### **Is my activity tracked?**
No tracking or analytics. The app is fully client-side with no server-side logging.

### **Can I use this offline?**
Once files are downloaded, you can view them offline. The app itself requires internet to browse.

---

## 📞 Support & Contact

For issues, feature requests, or questions:
- **GitHub Issues:** [Report a bug](https://github.com/aakashpuree/Com.Eng-notes/issues)
- **Email:** Reach out through GitHub profile
- **Discussions:** Participate in repository discussions

---

## 🚦 Project Status

- ✅ Core features complete
- ✅ Mobile responsive
- ✅ Production ready
- 🔄 Actively maintained
- 📋 Open for feature requests

**Last Updated:** June 2026
**Version:** 1.0.0

---

<div align="center">

### ⭐ If this project helped you, please consider giving it a star!

**Built with ❤️ for students who want better learning tools**

</div>
