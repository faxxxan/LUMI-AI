# Project AIRI-AI

<img width="100%" alt="banner" src="assets/banner.png" />

<p align="center">
  <a href="https://discord.gg/TgQ3Cu2F7A"><img src="https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fdiscord.com%2Fapi%2Finvites%2FTgQ3Cu2F7A%3Fwith_counts%3Dtrue&query=%24.approximate_member_count&suffix=%20members&logo=discord&logoColor=white&label=&color=7389D8&labelColor=6A7EC2"></a>
  <a href="https://github.com/faxxxan/AIRI-AI/blob/main/LICENSE"><img src="https://img.shields.io/github/license/faxxxan/AIRI-AI.svg?style=flat&colorA=080f12&colorB=1fa669"></a>
  <a href="https://x.com/proj_airi"><img src="https://img.shields.io/badge/%40proj__airi-black?style=flat&logo=x&labelColor=%23101419&color=%232d2e30"></a>
</p>

<h1 align="center">Project AIRI-AI</h1>

<p align="center">An advanced LLM-powered virtual character platform featuring AI-driven conversational agents with VRM 3D character models, real-time voice interaction, and cross-platform support.</p>

---

## 🎭 Meet the Characters

<table align="center" border="0">
  <tr>
    <td align="center" width="250">
      <img src="https://via.placeholder.com/200x200/1a1a2e/f0f0f0?text=AIRI" alt="AIRI" width="150" height="150" style="border-radius: 50%;">
      <h3>AIRI</h3>
      <p><i>The Elegant Scholar</i></p>
      <p>A refined anime-style character with sophisticated presence. Perfect for formal interactions and academic discussions.</p>
    </td>
    <td align="center" width="250">
      <img src="https://via.placeholder.com/200x200/2d4a3e/f0f0f0?text=KIRA" alt="KIRA" width="150" height="150" style="border-radius: 50%;">
      <h3>KIRA</h3>
      <p><i>The Energetic Spirit</i></p>
      <p>A vibrant character with dynamic personality. Great for casual conversations and energetic interactions.</p>
    </td>
  </tr>
  <tr>
    <td align="center" width="250">
      <img src="https://via.placeholder.com/200x200/f5d742/333333?text=NOVA" alt="NOVA" width="150" height="150" style="border-radius: 50%;">
      <h3>NOVA</h3>
      <p><i>The Warm Companion</i></p>
      <p>A cheerful character with a warm heart. Ideal for friendly conversations and emotional support.</p>
    </td>
    <td align="center" width="250">
      <img src="https://via.placeholder.com/200x200/4a1942/f0f0f0?text=LUMI" alt="LUMI" width="150" height="150" style="border-radius: 50%;">
      <h3>LUMI</h3>
      <p><i>The Mysterious Elegance</i></p>
      <p>A captivating character with an air of mystery. Perfect for deep conversations and creative storytelling.</p>
    </td>
  </tr>
</table>

---

## ✨ Key Features

### 🤖 AI-Powered Characters
- **LLM Integration**: Powered by state-of-the-art language models for natural, context-aware conversations
- **VRM 3D Models**: Beautiful anime-style 3D character models with expressive animations
- **Real-time Voice**: Speech synthesis and recognition for voice interactions

### 🎮 Cross-Platform Support
- **Web Application**: Full-featured web interface (`stage-web`)
- **Desktop App**: Electron-based desktop client (`stage-tamagotchi`)
- **Mobile Apps**: iOS and Android support via Capacitor (`stage-pocket`)

### 🔧 Developer-Friendly
- **Component System**: Extensible plugin architecture for custom components
- **OpenTelemetry**: Built-in observability with IO tracing and metrics
- **Hot Module Replacement**: Fast development with Vite

### 🎨 UI/UX
- **Vue 3 + TypeScript**: Modern reactive framework with type safety
- **UnoCSS**: Utility-first CSS with instant HMR
- **Responsive Design**: Adaptive layouts for all screen sizes

---

## 🛠️ Tech Stack

### Core Technologies
| Category | Technologies |
|----------|--------------|
| **Frontend** | Vue 3, TypeScript, Vite, UnoCSS |
| **Desktop** | Electron, Tauri (legacy) |
| **Mobile** | Capacitor, Kotlin, Swift |
| **Backend** | Hono, PostgreSQL, Redis |
| **AI/ML** | WebGPU Inference, LLM APIs, STT/TTS |
| **Monitoring** | OpenTelemetry, PostHog |
| **Database** | Drizzle ORM, Better Auth |
| **Testing** | Vitest |

### Project Structure
```
airi/
├── apps/
│   ├── stage-web/          # Web application
│   ├── stage-tamagotchi/    # Desktop Electron app
│   ├── stage-pocket/        # Mobile iOS/Android app
│   ├── component-calling/   # Plugin system
│   ├── server/              # Backend API server
│   └── ui-server-auth/      # Authentication server
├── packages/
│   ├── stage-ui/            # Core UI components
│   ├── stage-ui-three/      # Three.js bindings
│   ├── stage-pages/         # Shared page layouts
│   ├── stage-shared/        # Shared utilities
│   ├── i18n/                # Internationalization
│   ├── ui/                  # Primitive components
│   └── server-runtime/      # Server SDK
├── services/                # Backend services
├── plugins/                 # Plugins for extensions
└── docs/                   # Documentation
```

---

## 🚀 Installation

### Prerequisites
- Node.js 20+
- pnpm 9+
- PostgreSQL 15+
- Redis 7+

### Quick Start

```bash
# Clone the repository
git clone https://github.com/faxxxan/AIRI-AI.git
cd AIRI-AI

# Install dependencies
pnpm install

# Configure environment variables
cp .env.example .env
# Edit .env with your database and API keys

# Start development server
pnpm dev
```

### Environment Variables

Create a `.env` file with the following variables:

```env
# Database
DATABASE_URL=postgresql://user:password@localhost:5432/airi

# Redis
REDIS_URL=redis://localhost:6379

# Authentication
BETTER_AUTH_SECRET=your-secret-key
AUTH_GOOGLE_CLIENT_ID=your-google-client-id
AUTH_GOOGLE_CLIENT_SECRET=your-google-client-secret
AUTH_GITHUB_CLIENT_ID=your-github-client-id
AUTH_GITHUB_CLIENT_SECRET=your-github-client-secret
```

### Building for Production

```bash
# Build all applications
pnpm build

# Build specific app
pnpm -F @proj-airi/stage-web build
```

---

## 📖 Usage

### Web Application
Access the web interface at `http://localhost:5173` after running `pnpm dev`.

### Desktop Application
```bash
# Development mode
pnpm dev:tamagotchi

# Build executable
pnpm build:tamagotchi
```

### Mobile Development
```bash
# iOS
pnpm dev:pocket:ios

# Android
pnpm dev:pocket:android
```

---

## 🎯 Available Scripts

| Command | Description |
|---------|-------------|
| `pnpm dev` | Start development server |
| `pnpm build` | Build all apps and packages |
| `pnpm test` | Run tests with coverage |
| `pnpm lint` | Lint code |
| `pnpm typecheck` | Type-check all packages |

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'feat: add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct and the submission process.

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Copyright (c) 2024-PRESENT Neko Ayaka and the AIRI-AI contributors.

---

## 🙏 Acknowledgments

- **Original Project**: [moeru-ai/airi](https://github.com/moeru-ai/airi) - The foundation of this project
- **VRM Models**: Thanks to VRM consortium for the 3D character standard
- **Contributors**: All contributors who have helped improve this project

---

## 📬 Contact

- Discord: [Join our server](https://discord.gg/TgQ3Cu2F7A)
- Twitter: [@proj_airi](https://x.com/proj_airi)
- Email: airi@moeru.ai

---

<p align="center">
  Made with ❤️ by the AIRI-AI Team
</p>
