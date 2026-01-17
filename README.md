# Wallet Forge

> 100% client-side wallet data preparation tool with enterprise-grade validation

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

## 🔥 Features

### Security First
- 🔒 **100% Client-Side** — Zero backend, zero network requests
- 🔒 **No Data Storage** — Nothing saved to disk or cloud
- 🔒 **Offline Ready** — Works without internet connection
- 🔒 **Open Source** — Fully auditable single HTML file

### Validation
- ✅ **EIP-55 Checksum** — Proper Ethereum address validation
- ✅ **Private Key Format** — 64-char hex with optional 0x prefix
- ✅ **Real-Time Errors** — Shows exact line numbers of invalid entries
- ✅ **Count Mismatch Detection** — Warns when PKs ≠ Addresses

### Data Processing
- 🧹 **Auto-Clean** — Removes labels, quotes, and extra whitespace
- 🎲 **Shuffle** — Fisher-Yates randomization for security
- 🔄 **Deduplicate** — Remove duplicate wallet pairs
- 📏 **Normalize** — Lowercase and trim all entries

### Import/Export
- 📂 **JSON** — Import/export structured wallet data
- 📊 **CSV** — Standard spreadsheet format
- 📄 **TXT** — Plain text lists (one per line)
- 💾 **Individual Downloads** — Export keys or addresses separately

## 🚀 Quick Start

### Use Online
Visit the deployed version: [wallet-forge.vercel.app](https://wallet-forge.vercel.app)

### Use Locally
1. Download `index.html`
2. Open in any browser
3. No installation required

### Deploy Your Own

#### Vercel
```bash
git clone https://github.com/yourusername/wallet-forge
cd wallet-forge
vercel deploy
```

#### GitHub Pages
```bash
git clone https://github.com/yourusername/wallet-forge
cd wallet-forge
# Enable Pages in repo settings
git push origin main
```

#### Netlify
- Visit [app.netlify.com/drop](https://app.netlify.com/drop)
- Drag and drop `index.html`
- Done!

## 📖 Usage

### Basic Workflow
1. **Import or paste** wallet data (keys, addresses, or both)
2. **Validation runs automatically** — see errors in real-time
3. **Process as needed** — clean, shuffle, dedupe
4. **Export** in your preferred format

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

### Shuffle Example
Use before exporting to randomize wallet order:
```bash
🔀 Shuffle → Exports in random order
```
Perfect for farming, testing, or security purposes.

## 🛡️ Security Model

### What This Tool Does NOT Do
- ❌ No API calls
- ❌ No analytics
- ❌ No cookies
- ❌ No localStorage (without explicit action)
- ❌ No external scripts

### Audit Trail
- Single HTML file (~15KB)
- No build process
- No dependencies
- Fully inspectable source

### Safe For
- ✅ Private key management
- ✅ Airdrop preparation
- ✅ Multi-wallet operations
- ✅ Dev/test workflows

## 🎯 Use Cases

### Airdrop Farming
- Import wallet sets
- Validate all addresses
- Shuffle for randomness
- Export for bot consumption

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
- **~15KB** uncompressed
- **~6KB** gzipped
- Single file deployment

### Browser Support
- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- All modern browsers

### Standards
- EIP-55 address checksum
- RFC 4180 CSV format
- JSON structured output

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

### CSV Format
```csv
private_key,address
"0x...","0x..."
```

### TXT Format
```
0x... (one per line)
```

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

- [Report Bug](https://github.com/yourusername/wallet-forge/issues)
- [Request Feature](https://github.com/yourusername/wallet-forge/issues)
- [Documentation](https://github.com/yourusername/wallet-forge/wiki)

## ⚠️ Disclaimer

This tool handles sensitive data (private keys). While it runs entirely client-side with no network access:
- Always verify the source
- Use on a secure machine
- Never share private keys
- Test with small amounts first

**Use at your own risk. No warranties provided.**

---

Made with 🔥 by the community
