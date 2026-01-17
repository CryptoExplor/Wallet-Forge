# Wallet Forge v1.2.0 - Trust-Hardened Release 🔒

**Release Date:** January 2026
**Deployment:** [wallet-forge.vercel.app](https://wallet-forge.vercel.app)

---

## 🎯 Overview

Wallet Forge v1.2 is a **trust-hardened** release focused on security, validation accuracy, and offline capability. This version removes all external dependencies and adds enterprise-grade features while maintaining our core principle: **100% client-side, zero network calls**.

---

## 🔥 What's New

### Security & Trust
- ✅ **Proper EIP-55 Checksum Validation** - Real keccak256 validation using local `js-sha3`
- ✅ **Offline-First Architecture** - Removed all CDN dependencies, runs 100% offline
- ✅ **Content Security Policy** - CSP headers block any accidental network calls
- ✅ **Network Status Indicator** - Real-time offline/online status display
- 🔥 **Burn Session Feature** - Nuclear option to clear all data + reload

### Validation Improvements
- ✅ **Line-by-Line Error Detection** - Shows exact line numbers of invalid entries
- ✅ **Zero-Key Detection** - Prevents all-zero private keys (security risk)
- ✅ **Count Mismatch Warnings** - Alerts when PK count ≠ Address count
- ✅ **Real-Time Validation** - As-you-type feedback with error highlighting

### Export Flexibility (New in v1.2)
Four export format presets for different workflows:
- **Default** - `private_key, address` (full CSV)
- **Keys Only** - Private keys (one per line)
- **Addresses Only** - Addresses (one per line)  
- **Indexed** - With row numbers for batch tracking

Perfect for bot integration, ethers.js scripts, and automation workflows.

### Data Processing
- 🧹 **Auto-Clean** - Removes labels, quotes, punctuation
- 🎲 **Fisher-Yates Shuffle** - Cryptographically sound randomization
- 🔄 **Smart Deduplication** - Removes duplicate wallet pairs
- 📏 **Normalize** - Lowercase + trim (enabled by default)

---

## 📦 File Size

- **HTML:** ~21KB uncompressed (~8KB gzipped)
- **sha3.min.js:** ~5.6KB
- **Total:** Single-file deployment, zero build process

---

## 🛡️ Security Model

### What This Version Does NOT Do
- ❌ No API calls
- ❌ No analytics
- ❌ No cookies
- ❌ No external CDN scripts
- ❌ No localStorage (except burn session)
- ❌ No telemetry of any kind

### Trust Verification
```bash
# Download index.html
# Disconnect from internet
# Open in browser
# Tool works perfectly ✅
```

All code is auditable in a single HTML file + one local cryptography library.

---

## 🎯 Use Cases

### Airdrop Farming
- Import wallet sets from multiple sources
- Validate all addresses (EIP-55 checksum)
- Shuffle for operational security
- Export in bot-ready formats

### Development & Testing
- Clean messy CSV exports from exchanges
- Normalize address formats
- Prepare test wallet arrays
- Generate structured data for scripts

### Bot Integration (New)
- Export keys-only for ethers.js signer arrays
- Export indexed format for batch tracking
- Export addresses for recipient lists
- Prep data pipeline before automation

### Portfolio Management
- Merge wallet data from multiple tools
- Remove duplicates intelligently
- Validate checksums before use
- Export unified lists

---

## 📋 Changelog

### Added
- EIP-55 checksum validation with proper keccak256
- Four export format presets (default, keys-only, addresses-only, indexed)
- Burn session button (clears all data + reloads)
- Network status indicator (offline safe / online warnings)
- Content Security Policy meta tag
- Version badge in UI
- Zero-key detection

### Changed
- Removed CDN dependency (js-sha3 now served locally)
- Improved error messages with exact line numbers
- Enhanced validation stats display
- Better visual feedback for errors (red borders)
- Stricter security headers in deployment

### Fixed
- Checksum validation now uses real keccak256 (not pseudo-hash)
- Private key validation rejects all-zero keys
- Count mismatch detection more accurate
- CSV parsing handles more edge cases

---

## 🚀 Deployment

### Vercel (Recommended)
```bash
git clone https://github.com/CryptoExplor/Wallet-Forge
cd Wallet-Forge
vercel deploy --prod
```

### Local (Offline)
```bash
# Download index.html and sha3.min.js
# Open index.html in any browser
# Works 100% offline
```

### GitHub Pages
```bash
# Enable Pages in repo settings
# Source: main branch → /public folder
# Deploy automatically on push
```

---

## 📝 Files Included

- `public/index.html` - Complete application
- `public/sha3.min.js` - Local cryptography library
- `README.md` - Full documentation
- `LICENSE` - MIT License
- `vercel.json` - Deployment config with security headers
- `.gitignore` - Standard exclusions

---

## 🤝 Contributing

Contributions welcome! Please:
1. Fork the repo
2. Create a feature branch
3. Test offline mode
4. Submit a PR

**Guidelines:**
- Keep it client-side only
- No external dependencies
- Maintain security-first approach
- Add tests for validation logic

---

## ⚠️ Security Disclaimer

This tool handles **sensitive data** (private keys). While it runs entirely client-side:
- Always verify the source code
- Use on a secure, offline machine when possible
- Never share private keys
- Test with small amounts first
- Audit the code yourself before trusting it

**Use at your own risk. No warranties provided.**

---

## 🔗 Links

- **Live App:** [wallet-forge.vercel.app](https://wallet-forge.vercel.app)
- **Repository:** [github.com/CryptoExplor/Wallet-Forge](https://github.com/CryptoExplor/Wallet-Forge)
- **Issues:** [Report bugs or request features](https://github.com/CryptoExplor/Wallet-Forge/issues)
- **License:** MIT

---

## 📊 Comparison to v1.1

| Feature | v1.1 | v1.2 |
|---------|------|------|
| **Checksum Validation** | Basic format check | Real EIP-55 with keccak256 |
| **Export Formats** | 1 (default) | 4 (default, keys, addresses, indexed) |
| **Offline Capability** | Partial (CDN dependency) | 100% (local sha3) |
| **Burn Session** | ❌ | ✅ |
| **Network Indicator** | ❌ | ✅ |
| **CSP Protection** | ❌ | ✅ |
| **Zero-Key Detection** | ❌ | ✅ |
| **Line Error Numbers** | ❌ | ✅ |

---

## 🎯 What's Next?

v1.2 is feature-complete for core wallet data preparation. Future development will focus on:

**Potential v1.3 Features:**
- Export presets for popular frameworks (ethers.js, hardhat)
- Profile management (local storage only)
- Advanced filtering tools
- Column alignment helpers

**What We Won't Add:**
- ❌ Wallet connect / signing UI
- ❌ RPC calls or balance checks
- ❌ Backend or analytics
- ❌ Cloud storage

Staying **static, offline, and auditable** is what makes Wallet Forge trustworthy.

---

**v1.2 - Made with 🔥 by CryptoExplor**

*Trust through transparency. Security through simplicity.*
