
# NEXUS Shield | Enterprise Security Orchestrator

**NEXUS** is a high-performance, self-hosted security middleware for Node.js applications. It provides enterprise-grade protection against DDoS attacks, protocol abuse, and unauthorized access through a unified, intelligent firewall system.

## 🚀 Installation & Setup

### 1. Prerequisites
- **Node.js**: v18.0.0 or higher
- **NPM/Yarn**: Latest version
- **Operating System**: Linux (Recommended), Windows, or macOS

### 2. Fast Installation
Run this command in the directory where you want Nexus to be installed.

**All Terminals (Bash, PowerShell, CMD):**
```bash
git clone https://github.com/AndrewMack1/nexus.git nexus
cd nexus
npm install
```

**Force Update (If folder already exists):**
If you have an old version, just delete the `nexus` folder manually and run the command above.

Or, if you are using the dist build directly:

```bash
node nexus.js setup
```

Follow the interactive setup wizard to configure your admin credentials and bind the security engine to your application.

### 3. Activation
On first launch, you will be prompted for an **Activation Key**.
- Keys are managed via your private **Nexus Backend**.
- Ensure your backend is running on `http://localhost:8080` (or your configured remote URL).
- Keys are tied to the hardware UUID of the server they are activated on.

## 🛡️ Core Features

- **Intelligent Firewall**: Analyzes traffic patterns to block L7 DDoS attempts and burst attacks.
- **Console Dashboard**: A real-time web interface for monitoring traffic, latency, and threats.
- **Dynamic Ban System**: Automatically mitigates threats with temporary or permanent bans.
- **Request Inspection**: Deep packet inspection to filter malicious payloads and SQL injection attempts.
- **Obfuscated Core**: The production build is hardened to prevent tampering and reverse engineering.

## 🔧 Configuration

Nexus configurations are stored in `nexus/config/nexus.json`. You can modify security rules, rate limits, and whitelists directly or via the Admin Dashboard.

```json
{
  "security": {
    "rateLimit": { "windowMs": 60000, "maxRequests": 300 },
    "burstLimit": { "windowMs": 2000, "maxRequests": 50 }
  }
}
```

## 📦 Deployment

To start Nexus in production mode:

```bash
npm start
```

Or directly via Node:

```bash
node nexus.js start
```

## 📜 License
Proprietary software. Unauthorized distribution or modification is strictly prohibited.
Copyright © 2026 Nexus Enterprise. All rights reserved.
