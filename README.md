# Static Web Page Personalizer

A modern, fast, and aesthetically pleasing static web page template built with Astro. Designed specifically for generating personalized landing pages and dynamic image galleries for clients.

## ✨ Features

- **Astro Powered**: Ultra-fast static site generation.
- **Modern Aesthetics**: Built-in glassmorphism, smooth animations, and curated gradients.
- **Cloudflare Ready**: Configured for instant deployment to Cloudflare Pages.
- **Componentized**: Modular `Hero.astro` and `Gallery.astro` setups.

## 🚀 Getting Started

1. **Install dependencies:**
   ```bash
   npm install
   ```
2. **Start the development server:**
   ```bash
   npm run dev
   ```
3. **Build the site for production:**
   ```bash
   npm run build
   ```

## ☁️ Deploying to Cloudflare Pages

This project is configured to output standard static HTML, making it 100% compatible with Cloudflare Pages out of the box.

### Method 1: Git Integration (Recommended)
1. Push this repository to GitHub/GitLab.
2. Go to your [Cloudflare Dashboard](https://dash.cloudflare.com/) > **Workers & Pages**.
3. Click **Create application** > **Pages** > **Connect to Git**.
4. Select your repository.
5. Setup the build settings:
   - **Framework preset:** Astro
   - **Build command:** `npm run build`
   - **Build output directory:** `dist`
6. Click **Save and Deploy**. Once deployed, you can assign a custom **Public Domain** under the Custom Domains tab.

### Method 2: Wrangler CLI
If you prefer to deploy directly from your terminal:
1. Install Wrangler globally:
   ```bash
   npm install -g wrangler
   ```
2. Login to your Cloudflare account:
   ```bash
   npx wrangler login
   ```
3. Build and deploy:
   ```bash
   npm run build
   npx wrangler pages deploy dist --project-name="static-web-page-personalizer"
   ```

## 🎨 Customizing the Design
- **Global Styles & Variables**: `src/styles/global.css`
- **Layout**: `src/layouts/Layout.astro`
- **Theme Colors**: Modify the CSS variables in the `:root` block inside `global.css`.
