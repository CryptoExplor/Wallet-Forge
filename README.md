# Wallet Forge

> 100% client-side wallet data preparation tool with enterprise-grade validation

<div align="center">

[![Version](https://img.shields.io/badge/version-1.2.0-blue.svg)](https://github.com/CryptoExplor/Wallet-Forge/releases/tag/v1.2.0)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Vercel](https://img.shields.io/badge/deployed%20on-vercel-black)](https://wallet-forge.vercel.app)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

[![Offline](https://img.shields.io/badge/offline-capable-green)](https://wallet-forge.vercel.app)
[![No Tracking](https://img.shields.io/badge/tracking-none-green)](https://github.com/CryptoExplor/Wallet-Forge)
[![No Backend](https://img.shields.io/badge/backend-none-green)](https://github.com/CryptoExplor/Wallet-Forge)

[![EIP-55](https://img.shields.io/badge/EIP--55-validated-blue)](https://eips.ethereum.org/EIPS/eip-55)
[![Security](https://img.shields.io/badge/security-CSP%20protected-blue)](https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP)

</div>

## 🔥 Features

### Security First
- 🔒 **100% Client-Side** — Zero backend, zero network requests
- 🔒 **No External Dependencies** — All code runs locally
- 🔒 **No Data Storage** — Nothing saved to disk or cloud
- 🔒 **Offline Ready** — Works without internet connection
- 🔒 **Open Source** — Fully auditable single HTML file
- 🔥 **Burn Session** — Nuclear option to clear all data

### Validation (v1.2)
- ✅ **EIP-55 Checksum** — Proper Ethereum address validation
- ✅ **Private Key Format** — 64-char hex with optional 0x prefix
- ✅ **Real-Time Errors** — Shows exact line numbers of invalid entries
- ✅ **Count Mismatch Detection** — Warns when PKs ≠ Addresses
- ✅ **Zero-Key Detection** — Prevents all-zero private keys

### Data Processing
- 🧹 **Auto-Clean** — Removes labels, quotes, and extra whitespace
- 🎲 **Shuffle** — Fisher-Yates randomization for security
- 🔄 **Deduplicate** — Remove duplicate wallet pairs
- 📏 **Normalize** — Lowercase and trim all entries

### Export Formats (v1.2)
- 📋 **Default** — `private_key, address` (CSV)
- 🔑 **Keys Only** — Private keys (one per line)
- 🏠 **Addresses Only** — Addresses (one per line)
- 🔢 **Indexed** — With row numbers for tracking

### Import/Export
- 📂 **JSON** — Import/export structured wallet data
- 📊 **CSV** — Standard spreadsheet format
- 📄 **TXT** — Plain text lists (one per line)
- 💾 **Individual Downloads** — Export keys or addresses separately

## 🚀 Quick Start

### Use Online
Visit the deployed version: **[wallet-forge.vercel.app](https://wallet-forge.vercel.app)**

### Use Locally (Recommended for Maximum Security)
```bash
# 1. Clone the repository
git clone https://github.com/CryptoExplor/Wallet-Forge
cd Wallet-Forge/public

# 2. Disconnect from internet (optional but recommended)

# 3. Open in browser
open index.html  # macOS
start index.html # Windows
xdg-open index.html # Linux
```

**Works 100% offline** — no internet required after download.

### Deploy Your Own

#### Vercel (Recommended)
```bash
git clone https://github.com/CryptoExplor/Wallet-Forge
cd Wallet-Forge
vercel deploy --prod
```

#### GitHub Pages
```bash
git clone https://github.com/CryptoExplor/Wallet-Forge
cd Wallet-Forge
# Enable Pages: Settings → Pages → Source: main → Folder: /public
git push origin main
```

#### Netlify Drop
1. Visit [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag the `public` folder
3. Done!

## 📖 Usage

### Basic Workflow
1. **Import or paste** wallet data (keys, addresses, or both)
2. **Validation runs automatically** — see errors in real-time
3. **Process as needed** — clean, shuffle, dedupe
4. **Select export format** — choose the output you need
5. **Export** in your preferred format

### Validation Example
```
Input:
0x742d35Cc6634C0532925a3b844Bc9e7595f0bEb  ❌ Invalid (missing char)
0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045  ✅ Valid

Result:
✓ Valid: 1  ✗ Invalid: 1
Bad lines: 1
```

### Processing Options
- **Remove Duplicates** — Enabled by default
- **Normalize** — Lowercase + trim (enabled by default)
- **Pad Empty Values** — Fill mismatched rows with blanks

### Export Presets (New in v1.2)
Perfect for bot integration:
- **Default** — Full wallet pairs for record keeping
- **Keys Only** — For ethers.js signer arrays
- **Addresses Only** — For recipient lists
- **Indexed** — For batch operations with tracking

### Burn Session (New in v1.2)
Nuclear option for maximum security:
```
🔥 Burn Session → Clears all data + reloads page
```
Use after sensitive operations.

## 🔐 Security Model

Wallet Forge is designed to be maximally safe by default:

### Core Principles
- **Runs entirely in your browser** — No server-side processing
- **No backend** — Zero API calls, zero data transmission
- **No analytics** — Zero tracking or telemetry
- **No wallet connections** — Doesn't interact with MetaMask, WalletConnect, etc.
- **No signing or transaction logic** — Pure data preparation only
- **Can be used fully offline** — Download once, use forever

### Maximum Security Usage

For maximum security when handling sensitive data:

1. **Download the files** (`index.html` + `sha3.min.js`)
2. **Disconnect from the internet** (turn off WiFi/unplug ethernet)
3. **Open in browser** (works perfectly offline)
4. **Use Wallet Forge normally** (import, validate, export)
5. **Burn session when done** (clears all data + reloads)

### What This Tool Does NOT Do
- ❌ No API calls to any server
- ❌ No external CDN dependencies (v1.2+)
- ❌ No analytics, cookies, or tracking
- ❌ No localStorage (except burn session)
- ❌ No wallet signing or transactions
- ❌ No network requests of any kind

### Trust Verification

Verify it yourself:
```bash
# 1. Download the app
git clone https://github.com/CryptoExplor/Wallet-Forge
cd Wallet-Forge/public

# 2. Disconnect from internet
# (turn off WiFi or unplug ethernet)

# 3. Open in browser
open index.html

# 4. Tool works perfectly offline ✅
```

**See [SECURITY.md](SECURITY.md) for complete verification guide.**

### Audit Trail
- Single HTML file (~21KB)
- Local crypto library (sha3.min.js ~5.6KB)
- No build process
- No obfuscation
- Fully inspectable source code
- Content Security Policy enforced

### Safe For
- ✅ Private key management
- ✅ Airdrop preparation
- ✅ Multi-wallet operations
- ✅ Dev/test workflows
- ✅ Offline environments
- ✅ Air-gapped systems

## 🎯 Use Cases

### Airdrop Farming
- Import wallet sets
- Validate all addresses
- Shuffle for randomness
- Export for bot consumption

### Bot Integration (v1.2)
- Export keys-only for ethers.js
- Export indexed for batch tracking
- Export addresses for recipient lists
- Prep data before automation

### Development
- Clean messy CSV exports
- Normalize address formats
- Prepare test wallets
- Generate structured data

### Portfolio Management
- Merge multiple sources
- Remove duplicates
- Validate checksums
- Export unified lists

## 🔧 Technical Details

### File Size
- **~21KB** uncompressed
- **~8KB** gzipped
- Single file deployment

### Browser Support
- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- All modern browsers

### Standards
- EIP-55 address checksum (js-sha3)
- RFC 4180 CSV format
- JSON structured output

### Network Status Indicator (v1.2)
- Shows `✅ Offline Safe` when disconnected
- Shows `⚠️ Online (no network calls)` when connected
- Real-time status updates

## 📝 File Formats

### JSON Structure
```json
[
  {
    "private_key": "0x...",
    "address": "0x..."
  }
]
```

### CSV Formats

**Default:**
```csv
private_key,address
"0x...","0x..."
```

**Indexed (new in v1.2):**
```csv
index,private_key,address
1,"0x...","0x..."
```

**Keys Only:**
```
0x...
0x...
```

**Addresses Only:**
```
0x...
0x...
```

## 📋 Changelog

### v1.2 (Current) - Trust Hardening
- ✅ Proper EIP-55 checksum validation (js-sha3)
- ✅ Export format presets (4 modes)
- ✅ Burn Session button
- ✅ Network status indicator
- ✅ Removed CDN dependencies (fully offline)
- ✅ Zero-key detection

### v1.1 - Validation
- Real-time validation
- Line number error reporting
- Deduplication
- Shuffle function
- Count mismatch warnings

### v1.0 - Initial Release
- Basic import/export
- CSV/JSON support
- Auto-clean

## 🤝 Contributing

Contributions welcome! Please:
1. Fork the repo
2. Create a feature branch
3. Submit a PR

### Development
No build process needed:
```bash
# Edit index.html directly
# Test in browser
# Commit changes
```

## 📄 License

MIT License - see [LICENSE](LICENSE) file

## 🔗 Links

- **Live App:** [wallet-forge.vercel.app](https://wallet-forge.vercel.app)
- **Repository:** [github.com/CryptoExplor/Wallet-Forge](https://github.com/CryptoExplor/Wallet-Forge)
- **Report Bug:** [GitHub Issues](https://github.com/CryptoExplor/Wallet-Forge/issues)
- **Request Feature:** [GitHub Issues](https://github.com/CryptoExplor/Wallet-Forge/issues)
- **Security Guide:** [SECURITY.md](SECURITY.md)

## ⚠️ Disclaimer

This tool handles **sensitive data** (private keys). While it runs entirely client-side with no network access:

- Always verify the source code before use
- Use on a secure, malware-free machine
- Never share private keys with anyone
- Test with small amounts first
- **For maximum security: download and run offline**

See [SECURITY.md](SECURITY.md) for complete verification instructions.

**Use at your own risk. No warranties provided.**

---

**v1.2** — Made with 🔥 by CryptoExplor

*Trust through transparency. Security through simplicity.*
