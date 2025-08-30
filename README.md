# Balanced Pitch - AI Ethics in Music

A modern, interactive website advocating for artists' rights and ethical AI standards in the music industry. Built with React, featuring sophisticated animations, custom music player, and engaging user experience.

## 🎯 Overview

**Balanced Pitch** is a company that champions artists' rights and establishes ethical AI standards in the music industry. Our mission is to ensure future generations can thrive in an AI-shaped music landscape while protecting artists' intellectual property.

### Key Features
- 🎵 **Interactive Music Player** - Custom vinyl record interface with original tracks
- ✨ **Smooth Animations** - GSAP-powered scroll animations and page transitions
- 📱 **Responsive Design** - Modern UI that works on all devices
- 🎨 **Custom Typography** - Unique font families for brand identity
- 🌙 **Theme Support** - Light and dark theme variations
- 🎬 **Parallax Effects** - Engaging scroll-triggered animations

## 🛠 Tech Stack

- **Frontend Framework**: React 18
- **Build Tool**: Vite
- **Routing**: React Router DOM
- **Animations**: 
  - GSAP (GreenSock Animation Platform)
  - Framer Motion
  - Lenis (Smooth Scrolling)
- **Styling**: Custom CSS
- **Audio**: HTML5 Audio API
- **Package Manager**: npm

## 📁 Project Structure

```
balanced-pitch/
├── public/                 # Static assets
│   ├── home/              # Home page images
│   ├── about/             # About page images
│   ├── solutions/         # Solutions page images
│   ├── updates/           # Updates page images
│   ├── contact/           # Contact page images
│   ├── songs/             # Audio files and album art
│   ├── menu/              # Menu background images
│   └── logo.png           # Brand assets
├── src/
│   ├── components/        # Reusable components
│   │   ├── Footer/        # Site footer
│   │   ├── Menu/          # Navigation menu
│   │   ├── MusicPlayer/   # Custom music player
│   │   ├── ParallaxImage/ # Parallax image component
│   │   └── Transition/    # Page transition effects
│   ├── pages/             # Page components
│   │   ├── home/          # Home page
│   │   ├── about/         # About page
│   │   ├── solutions/     # Solutions page
│   │   ├── updates/       # Updates page
│   │   └── contact/       # Contact page
│   ├── assets/            # Fonts and other assets
│   ├── App.jsx            # Main app component
│   ├── App.css            # Global styles
│   ├── main.jsx           # App entry point
│   └── index.css          # Base styles
├── package.json           # Dependencies and scripts
├── vite.config.js         # Vite configuration
└── eslint.config.js       # ESLint configuration
```

## 🚀 Getting Started

### Prerequisites

- **Node.js** (version 16 or higher)
- **npm** (comes with Node.js)

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd balanced-pitch
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start development server**
   ```bash
   npm run dev
   ```

4. **Open your browser**
   Navigate to `http://localhost:5173` to view the application.

### Available Scripts

- `npm run dev` - Start development server with hot reload
- `npm run build` - Build for production
- `npm run preview` - Preview production build locally
- `npm run lint` - Run ESLint to check code quality

## 🎵 Music Player Features

The application includes a custom music player with:

- **Vinyl Record Interface** - Realistic vinyl record with flip animations
- **Original Tracks**:
  - "Dreamland" by Balanced Pitch
  - "Gameplay" by Balanced Pitch
- **Controls**: Play/pause, next/previous track
- **Auto-play**: Automatically plays next track when current ends
- **Visual Feedback**: Spinning animation when playing

## 🎨 Design System

### Typography
- **Primary Font**: FK Screamer (for headings)
- **Secondary Font**: PP Editorial New family (for body text)
  - Regular, Bold, Heavy, Thin, Ultralight variants

### Color Scheme
- **Light Theme**: Clean, modern aesthetic
- **Dark Theme**: Applied on specific pages (e.g., Updates page)

### Animations
- **Scroll Animations**: GSAP ScrollTrigger for scroll-based effects
- **Page Transitions**: Framer Motion for smooth page changes
- **Menu Animations**: Sophisticated open/close animations
- **Parallax Effects**: Depth-based scrolling animations

## 📱 Pages Overview

### Home (`/`)
- Hero section with company introduction
- Interactive music player
- News article preview
- Company mission statement

### About (`/about`)
- Company story and mission
- Team information
- Sign-up card for ethical AI advocacy
- Careers section

### Solutions (`/solutions`)
- Services and solutions offered
- Call-to-action sections
- Visual demonstrations

### Updates (`/updates`)
- News and updates section
- Article listings
- Dark theme implementation

### Contact (`/contact`)
- Contact information
- Contact form
- Location details

## 🚀 Deployment

### Production Build

1. **Build the application**
   ```bash
   npm run build
   ```

2. **Preview the build locally**
   ```bash
   npm run preview
   ```

### Server Deployment

#### Option 1: Static Hosting (Recommended)

The application is a static site that can be deployed to any static hosting service:

**Netlify:**
1. Connect your repository to Netlify
2. Set build command: `npm run build`
3. Set publish directory: `dist`
4. Deploy automatically on push

**Vercel:**
1. Connect your repository to Vercel
2. Framework preset: Vite
3. Deploy automatically on push

**GitHub Pages:**
1. Add to `package.json`:
   ```json
   {
     "homepage": "https://yourusername.github.io/balanced-pitch",
     "scripts": {
       "predeploy": "npm run build",
       "deploy": "gh-pages -d dist"
     }
   }
   ```
2. Install gh-pages: `npm install --save-dev gh-pages`
3. Deploy: `npm run deploy`

#### Option 2: Traditional Web Server

1. **Build the application**
   ```bash
   npm run build
   ```

2. **Upload contents of `dist/` folder** to your web server's public directory

3. **Configure server** to serve `index.html` for all routes (SPA routing)

**Apache (.htaccess):**
```apache
RewriteEngine On
RewriteBase /
RewriteRule ^index\.html$ - [L]
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule . /index.html [L]
```

**Nginx:**
```nginx
location / {
    try_files $uri $uri/ /index.html;
}
```

### Environment Variables

No environment variables are required for basic functionality. The application is self-contained.

## 🔧 Configuration

### Vite Configuration (`vite.config.js`)
- React plugin for Fast Refresh
- Optimized for production builds
- Asset handling for images and fonts

### ESLint Configuration (`eslint.config.js`)
- React-specific linting rules
- Hooks linting
- Refresh plugin for development

## 📦 Dependencies

### Production Dependencies
- `react` (^18.3.1) - UI framework
- `react-dom` (^18.3.1) - React DOM rendering
- `react-router-dom` (^7.0.1) - Client-side routing
- `framer-motion` (^11.11.17) - Animation library
- `gsap` (^3.12.5) - Advanced animations
- `lenis` (^1.1.17) - Smooth scrolling
- `@studio-freight/react-lenis` (^0.0.47) - React wrapper for Lenis

### Development Dependencies
- `@vitejs/plugin-react` (^4.3.3) - Vite React plugin
- `vite` (^5.4.10) - Build tool
- `eslint` (^9.13.0) - Code linting
- `@types/react` (^18.3.12) - TypeScript definitions

## 🎯 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Commit changes: `git commit -am 'Add feature'`
4. Push to branch: `git push origin feature-name`
5. Submit a pull request

## 📄 License

This project is proprietary software. All rights reserved.

## 📞 Support

For support and inquiries:
- Email: [contact@balancedpitch.com]
- Website: [https://balancedpitch.com]

---

**Balanced Pitch** - Shaping the Future of Music with AI
