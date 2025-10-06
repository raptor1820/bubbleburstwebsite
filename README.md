# 💥 BUBBLE BURST!

<div align="center">

**Break free from your filter bubble. See the other side of the story.**

[![Built with SvelteKit](https://img.shields.io/badge/Built%20with-SvelteKit-FF3E00?style=for-the-badge&logo=svelte&logoColor=white)](https://kit.svelte.dev/)
[![Powered by Bun](https://img.shields.io/badge/Powered%20by-Bun-000000?style=for-the-badge&logo=bun&logoColor=white)](https://bun.sh/)
[![Vercel Analytics](https://img.shields.io/badge/Analytics-Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://vercel.com/analytics)

[Live Demo](https://bubbleburst.ritwic.com) • [Report Bug](https://github.com/raptor1820/bubbleburstwebsite/issues) • [Request Feature](https://github.com/raptor1820/bubbleburstwebsite/issues)

</div>

---

## 🎯 What is Bubble Burst?

In today's digital age, we're increasingly trapped in echo chambers where we only see content that confirms our existing beliefs. **Bubble Burst** is a web application designed to combat this by showing you alternative perspectives on any news article.

Simply paste a URL of any news article, and Bubble Burst will find related articles from different sources and viewpoints, helping you:

- 🔍 **Discover** alternative perspectives on the same story
- 🧠 **Think critically** about the news you consume
- 🌐 **Explore** how different outlets cover the same events
- 💡 **Make informed** decisions based on multiple viewpoints

## ✨ Features

- **🚀 Lightning Fast**: Built with SvelteKit and Bun for optimal performance
- **🎨 Retro Design**: Nostalgic pixel-art aesthetic with smooth interactions
- **⌨️ Keyboard Shortcuts**: Press Enter to search instantly
- **📱 Responsive**: Works seamlessly on desktop and mobile devices
- **🔗 Direct Links**: Click any result to read the full article
- **🎯 Clean UI**: Minimalist interface that puts content first

## 🚀 Quick Start

### Prerequisites

- [Bun](https://bun.sh/) (recommended) or [Node.js](https://nodejs.org/) 18+

### Installation

```bash
# Clone the repository
git clone https://github.com/raptor1820/bubbleburstwebsite.git

# Navigate to the project directory
cd bubbleburstwebsite

# Install dependencies
bun install
# or: npm install
```

### Development

Start the development server:

```bash
bun run dev
# or: npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser to see the app.

### Building for Production

```bash
# Create a production build
bun run build

# Preview the production build
bun run preview
```

## 🛠️ Tech Stack

- **Framework**: [SvelteKit](https://kit.svelte.dev/) - Modern web framework with excellent performance
- **Runtime**: [Bun](https://bun.sh/) - Fast JavaScript runtime and toolkit
- **Styling**: Vanilla CSS with custom properties and Google Fonts
- **Analytics**: [Vercel Analytics](https://vercel.com/analytics) - Privacy-friendly analytics
- **Code Quality**: ESLint + Prettier for consistent code formatting

## 📁 Project Structure

```
bubbleburstwebsite/
├── src/
│   ├── routes/
│   │   ├── +page.svelte      # Main page component
│   │   └── Card.svelte        # Article card component
│   ├── lib/
│   │   └── index.js           # Utility functions
│   └── app.html               # HTML template
├── static/                    # Static assets
├── package.json               # Project dependencies
├── svelte.config.js           # SvelteKit configuration
└── vite.config.js             # Vite configuration
```

## 🎨 Design Philosophy

Bubble Burst features a distinctive **neobrutalist** design inspired by retro computing:

- **Press Start 2P** font for the pixel-art header
- **Varela Round** for clean, readable body text
- Warm **#FFEBCA** background for comfortable reading
- Bold black borders with shadow effects for depth
- Subtle hover animations for interactive feedback

## 🔌 API Integration

The application connects to the Bubble Burst API:

```
https://apibubbleburst.ritwic.com/?url=[ARTICLE_URL]
```

The API analyzes the provided article and returns related content from different sources and perspectives.

## 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Development Guidelines

```bash
# Run linting
bun run lint

# Format code
bun run format
```

## 📝 License

This project is open source and available for educational purposes.

## 🙏 Acknowledgments

- Built with [SvelteKit](https://kit.svelte.dev/)
- Fonts from [Google Fonts](https://fonts.google.com/)
- Inspired by the need for diverse perspectives in media consumption

## 📧 Contact

Ritwic - [@raptor1820](https://github.com/raptor1820)

Project Link: [https://github.com/raptor1820/bubbleburstwebsite](https://github.com/raptor1820/bubbleburstwebsite)

---

<div align="center">

**Made with ❤️ to promote critical thinking and diverse perspectives**

⭐ Star this repo if you found it helpful!

</div>

```

## Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

To create a production version of your app:

```bash
npm run build
```

You can preview the production build with `npm run preview`.

> To deploy your app, you may need to install an [adapter](https://kit.svelte.dev/docs/adapters) for your target environment.
