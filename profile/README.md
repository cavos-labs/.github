# Cavos Labs

> **Invisible Crypto Infrastructure for Starknet** - Bridging the gap between blockchain and mainstream apps

[![Website](https://img.shields.io/badge/Website-cavos.xyz-blue)](https://cavos.xyz)
[![Twitter](https://img.shields.io/badge/Twitter-@cavosxyz-1DA1F2)](https://x.com/cavosxyz)

## About Us

Cavos Labs builds infrastructure that makes interacting with Starknet seamless. We provide powerful SDKs and smart contract architectures that integrate gasless transactions, invisible wallets via OAuth (Apple/Google), and autonomous AI agent session keys directly into your applications.

### Our Mission
Remove the friction from Web3. No seed phrases, no wallet popups, just standard social logins and seamless on-chain execution powered by Starknet Account Abstraction and Enshrined Paymasters.

## 📦 What We're Building

### **Core Repositories**

- 🧠 **[cavos-skills](https://github.com/cavos-labs/cavos-skills)** - Comprehensive knowledge base for the Cavos React SDK — enabling AI agents to understand Starknet account abstraction via OAuth, session keys, and gasless transactions.
- 📱 **[react](https://github.com/cavos-labs/react)** - The core `@cavos/react` TypeScript library for managing in-app wallets seamlessly tied to social logins on Starknet.
- ⚛️ **[react-native](https://github.com/cavos-labs/react-native)** - Cavos React Native package bringing account abstraction and invisible wallets to mobile platforms.
- 📜 **[cavos](https://github.com/cavos-labs/cavos)** - The core Cairo smart contracts including our highly-optimized RSA signature verification and Account Abstraction logic.
- 🤖 **[agent](https://github.com/cavos-labs/agent)** - Web view interface for administering and managing agent Session Keys.
- 🚀 **[create-cavos-app](https://github.com/cavos-labs/create-cavos-app)** - Quickstart CLI and templates to bootstrap your Cavos-powered Starknet dApps instantly.
- 📖 **[docs](https://github.com/cavos-labs/docs)** - Official comprehensive documentation for integrating Cavos SDKs.

## 🛠 Features

- **OAuth Account Abstraction:** Deploy Starknet Smart Accounts entirely controlled by JWT tokens (Apple/Google).
- **Session Keys:** Issue granular session keys to allow AI agents or background services to perform transactions on your behalf without multiple prompts.
- **Gasless Transactions:** Built-in support for SNIP-29 Enshrined Paymaster standard, ensuring robust and decentralized transaction sponsorship.
- **Highly Optimized Cairo:** Industry-leading gas optimizations using Karatsuba algorithms for RSA signature verification on-chain.

## 💻 Integration Examples

### React App
```tsx
import { CavosProvider } from '@cavos/react';

export default function App({ children }) {
  return (
    <CavosProvider 
      appId="your_app_id"
      network="sepolia"
    >
      {children}
    </CavosProvider>
  );
}
```

## 📬 Get in Touch

- **Website**: [cavos.xyz](https://cavos.xyz)
- **Twitter**: [@cavosxyz](https://x.com/cavosxyz)

---

*Making Starknet invisible, one integration at a time.* ⚡
