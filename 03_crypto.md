# Crypto Track: Bitcoin, Ethereum, DeFi, Stablecoins, Rust and Solana, and Trading

Track 3 of 3 · Pranav's self-study roadmap · starts Thu 26 Nov 2026

This track rotates with Quant and Investing: one track per day, Sundays free for catch-up. The full calendar is at the bottom.

Everything here is free. The coding path goes from Python toy blockchains to Solidity on Ethereum, then Rust, then Solana programs with Anchor, and ends with crypto market data and trading.

Since you start at BitGo in January, Sessions C03 and C29 cover custody, multisig and key management, which is BitGo's core business. Check BitGo's personal trading policy before you trade any crypto with real money.

---

## 0. How to use this file

Each session is about 60 minutes: 25 minutes watching or reading, 30 minutes coding, 5 minutes of notes in `notes/crypto.md`.

Setup over the first sessions:
- Python environment: `hashlib` (built in), `ecdsa`, `requests`, `pandas`, `ccxt`.
- From C08: Remix IDE (browser) and then Foundry for Solidity.
- From C15: Rust via `rustup`, plus Rustlings.
- From C19: Solana CLI, Anchor, and [Solana Playground](https://beta.solpg.io) (runs in the browser, so you can start without installing anything).
- A MetaMask wallet and a Solana wallet (like Phantom) used only on testnets and devnet. Never put real funds in learning wallets.

Repo: `crypto-lab/` with `python/`, `solidity/`, `rust/`, `solana/`, `notes/` and `reports/`.

India rules worth knowing before any real trade: gains on crypto ("virtual digital assets") are taxed at a flat 30% plus cess, with 1% TDS on transfers, and losses can't be set off against other income. These rates were left unchanged in Budget 2026. Use an Indian exchange registered with FIU-IND, and confirm the current rules before trading.

---

## 1. Map of this world

| Layer | What it is | Sessions |
|---|---|---|
| Cryptography | Hashes, signatures, Merkle trees | C01 to C03 |
| Bitcoin | UTXOs, proof of work, scripts, wallets | C01 to C06 |
| Ethereum and EVM | Accounts, gas, smart contracts, Solidity | C07 to C09 |
| DeFi | AMMs, lending, oracles, flash loans, MEV | C10, C11 |
| Stablecoins | Fiat-backed, crypto-backed, algorithmic, and how they fail | C12 |
| Security | Common contract exploits | C13, C23 |
| Rust | The language behind Solana and much of crypto infrastructure | C15 to C18 |
| Solana | Accounts model, Sealevel, Anchor, PDAs, SPL tokens | C19 to C24 |
| Trading and data | Exchanges, perps, funding, on-chain analytics, market making | C05, C25 to C27 |
| Other chains, custody | L2s, bridges, MPC, multisig, HD wallets | C28, C29 |

---

## 2. Core resources

Foundations
- Bitcoin whitepaper: [bitcoin.org/bitcoin.pdf](https://bitcoin.org/bitcoin.pdf) (9 pages).
- Princeton "Bitcoin and Cryptocurrency Technologies" (Narayanan, Bonneau, Felten, Miller): free to audit on [Coursera](https://www.coursera.org/learn/cryptocurrency). The lectures are also on YouTube, and there's a free draft of the companion textbook.
- Mastering Bitcoin (Antonopoulos): free on GitHub at [bitcoinbook/bitcoinbook](https://github.com/bitcoinbook/bitcoinbook).

Ethereum, Solidity, DeFi
- Ethereum whitepaper: [ethereum.org/whitepaper](https://ethereum.org/whitepaper).
- Mastering Ethereum (Antonopoulos and Wood): free on GitHub at [ethereumbook/ethereumbook](https://github.com/ethereumbook/ethereumbook).
- Cyfrin Updraft (Patrick Collins): [updraft.cyfrin.io/courses](https://updraft.cyfrin.io/courses), entirely free. Start with Blockchain Basics, then Solidity and Foundry. It also has a [Solana course](https://updraft.cyfrin.io/courses/solana) covering native Rust and Anchor.
- UC Berkeley Decentralized Finance MOOC (Dawn Song, Christine Parlour and guests): course pages with YouTube playlists for each lecture, for example the [Fall 2024 syllabus](https://rdi.berkeley.edu/berkeley-defi/f24_syllabus). Topics include intro to blockchain, traditional finance, DEXs, lending, stablecoins, oracles, MEV, security, and derivatives.
- Uniswap whitepapers: [v2](https://app.uniswap.org/whitepaper.pdf) (constant product AMM) and [v3](https://uniswap.org/whitepaper-v3.pdf) (concentrated liquidity).
- Security games: [Ethernaut](https://ethernaut.openzeppelin.com) (each level is a broken contract you exploit), [Damn Vulnerable DeFi](https://www.damnvulnerabledefi.xyz), and [Speedrun Ethereum](https://speedrunethereum.com) for build challenges.

Stablecoins (papers, all free)
- "SoK: Stablecoin Designs, Risks, and the Stablecoin LEGO": [arXiv 2506.17622](https://arxiv.org/abs/2506.17622).
- "Stablecoins: Fundamentals, Emerging Issues, and Open Challenges": [arXiv 2507.13883](https://arxiv.org/abs/2507.13883).
- Kurovskiy and Rostova, "How Algorithmic Stablecoins Fail" (the Terra/UST collapse with transaction-level data): [PDF via Swiss National Bank seminar](https://snb.ch/dam/jcr:5140cb30-3c8c-433d-8619-0354b8f1036e/sem_2023_05_26_rostova.n.pdf).

Rust
- The Rust Programming Language ("the Book"): [doc.rust-lang.org/book](https://doc.rust-lang.org/book/).
- Let's Get Rusty, ["The Rust Lang Book" playlist](https://www.youtube.com/playlist?list=PLai5B987bZ9CoVR-QEIN9foz4QCJ0H2Y8), which goes through the Book chapter by chapter.
- [Rustlings](https://github.com/rust-lang/rustlings): small exercises you fix until they compile.
- Jon Gjengset's "Crust of Rust" series on YouTube, for later, when you want depth.

Solana
- Official [Solana Crash Course](https://solana.com/docs/video-guides/solana-crash-course) (11 videos, about 3 hours, from setup to shipping an Anchor program) and the [Developer Bootcamp 2026](https://solana.com/developers/bootcamp) (12 projects).
- Ackee Blockchain's [School of Solana](https://ackee.xyz/school-of-solana): free, runs in cohorts (apply for the next season), with materials on [GitHub](https://github.com/Ackee-Blockchain/school-of-solana) and the free [Solana Handbook](https://ackee.xyz/solana/book/).
- Solana's [Program Security course](https://solana.com/developers/courses/program-security/security-intro), modelled on Coral's Sealevel Attacks repository (github.com/coral-xyz/sealevel-attacks).

Markets, data, trading
- [ccxt](https://github.com/ccxt/ccxt): one Python library for public market data from almost every exchange.
- [Dune](https://dune.com): query blockchain data with SQL, free tier.
- mempool.space: watch Bitcoin blocks and fees live.
- [hftbacktest](https://github.com/nkaz001/hftbacktest): market making backtests on real crypto order book data. Shared with Quant track Q26.
- YouTube: Benjamin Cowen (Into the Cryptoverse) for data-driven cycle analysis, Coin Bureau for explainers on coins and sectors, and Whiteboard Crypto for short concept videos.

---

## 3. The sessions

### Block A · Cryptography and Bitcoin

#### C01 · Thu 26 Nov 2026 · Hashes and the Bitcoin whitepaper
- Read: the Bitcoin whitepaper, all of it.
- Watch: Princeton Week 1 (cryptographic hash functions, hash pointers, digital signatures).
- Code `python/c01_hash.py`: SHA-256 with `hashlib`. Show the avalanche effect (change 1 bit and see how many output bits change). Write a toy proof of work that finds a nonce so the hash starts with k zeros, and time it for k = 1 to 6. Plot time vs k. Each extra zero should take about 16 times longer, so check whether yours does.

#### C02 · Mon 30 Nov 2026 · Decentralization, consensus, UTXOs
- Watch: Princeton Weeks 2 and 3 (how Bitcoin achieves decentralization, mechanics of Bitcoin: transactions, Script, blocks, the P2P network).
- Code: a Merkle tree (build the root, generate and verify an inclusion proof) and a toy UTXO ledger that rejects double spends.

#### C03 · Thu 3 Dec 2026 · Keys, wallets, custody (BitGo territory)
- Watch: Princeton Week 4 (how to store and use bitcoins: hot vs cold storage, splitting keys, multisig, exchanges).
- Code: generate an ECDSA keypair on secp256k1 with the `ecdsa` library, sign and verify a message, and show that a changed message fails verification.
- Write: 5 bullets on why a custodian like BitGo uses multisig or MPC instead of one private key.

#### C04 · Mon 7 Dec 2026 · Mining, fees, supply
- Watch: Princeton Week 5 (mining, mining hardware, pools, incentives).
- Read: Mastering Bitcoin chapters on the network, the blockchain and mining.
- Practice: spend 10 minutes on mempool.space looking at fee rates, block fullness and the next block template.
- Code: plot Bitcoin's supply schedule (block reward halving every 210,000 blocks) up to the 21 million cap, and mark the halving dates.

#### C05 · Thu 10 Dec 2026 · How crypto markets work
- Learn: centralized exchanges vs DEXs, order books, spot vs perpetual futures, funding rates, liquidations, stablecoins as the quote currency, and market makers' role.
- Watch: one Benjamin Cowen video on Bitcoin market cycles and one Coin Bureau explainer on perpetual futures.
- Code: use `ccxt` to pull the BTC/USDT order book snapshot and recent trades from one exchange's public API (no account needed). Compute the spread, the depth within 0.1% of the mid, and the order book imbalance.

#### C06 · Mon 14 Dec 2026 · CHECKPOINT 1: Build a mini blockchain
Deliverable `python/minichain/` plus `reports/cp1_minichain.md`:
1. Blocks with header, previous hash, Merkle root, nonce and timestamp.
2. Signed transactions using your C03 keys, plus UTXO validation.
3. Proof of work with difficulty adjustment every N blocks.
4. Chain validation that rejects a tampered block.
5. A one-page explainer as if teaching it to a junior.

Report back: the repo link, plus what broke first when you tampered with a block.

### Block B · Ethereum, smart contracts, DeFi, stablecoins

#### C07 · Thu 17 Dec 2026 · Ethereum and the EVM
- Read: the Ethereum whitepaper, and Mastering Ethereum chapters on accounts, transactions, gas and the EVM.
- Watch: Cyfrin Updraft Blockchain Basics.
- Write: a table comparing Bitcoin's UTXO model with Ethereum's account model (state, parallelism, privacy, smart contracts).

#### C08 · Mon 21 Dec 2026 · Solidity basics
- Course: Cyfrin Updraft Solidity Smart Contract Development, the first sections (Simple Storage, types, functions).
- Practice: deploy a storage contract and a simple "fund me" contract in Remix to a testnet, then view your transaction on the block explorer.

#### C09 · Thu 24 Dec 2026 · Foundry and tokens
- Course: Cyfrin Updraft Foundry sections.
- Code: an ERC-20 token using OpenZeppelin, with Foundry tests for transfer, approve and transferFrom, plus one fuzz test.

#### C10 · Mon 28 Dec 2026 · DeFi I: AMMs
- Read: the Uniswap v2 whitepaper (constant product formula, fees, price oracle).
- Watch: the Berkeley DeFi lecture on DEXs and AMMs.
- Code (Python): a constant product AMM with fees. Simulate swaps, price impact vs trade size, and impermanent loss for a liquidity provider as the price moves from 0.5x to 2x. Plot impermanent loss vs price change.

#### C11 · Thu 31 Dec 2026 · DeFi II: lending, oracles, flash loans, MEV
- Watch: the Berkeley DeFi lectures on lending protocols, oracles and MEV.
- Learn: collateral ratios, liquidations, interest rate curves, why oracle manipulation causes most DeFi hacks, and what a flash loan makes possible.
- Code: simulate a lending pool. A 30% ETH price drop triggers liquidations, and you plot how many positions get liquidated at each price.

#### C12 · Mon 4 Jan 2027 · Stablecoins: all three kinds, and how they fail
- Read: the "SoK: Stablecoin Designs" paper (the overview and taxonomy sections), then Kurovskiy and Rostova's paper on the UST collapse.
- Learn: fiat-backed (USDC, USDT: reserves, attestations, redemption), crypto-collateralized (DAI/Sky: overcollateralization, liquidations) and algorithmic (UST: mint and burn against LUNA, and why that loop can become a death spiral).
- Code: simulate the UST/LUNA mechanism. Start with a redemption shock and watch LUNA supply explode as the peg breaks. Find the shock size that tips it over.

#### C13 · Thu 7 Jan 2027 · Smart contract security
- Play: Ethernaut levels 1 to 5.
- Learn: reentrancy, access control mistakes, integer issues, unchecked external calls, and front-running.
- Write: for each level, one sentence on the bug and one on the fix.

#### C14 · Mon 11 Jan 2027 · CHECKPOINT 2: Your own AMM
Deliverable `solidity/mini-amm/` plus `reports/cp2_amm.md`:
1. A constant product AMM in Solidity: addLiquidity, removeLiquidity, swap, and a 0.3% fee.
2. Foundry tests, including an invariant test that k never decreases.
3. Your Python impermanent loss simulation from C10, checked against the on-chain behaviour.
4. Read the Uniswap v3 whitepaper's concentrated liquidity section, and explain in a paragraph why v3 needed it.

Report back: test results, and your explanation of concentrated liquidity.

### Block C · Rust and Solana

#### C15 · Thu 14 Jan 2027 · Rust I: ownership
- Read and watch: Rust Book chapters 1 to 4 with the matching Let's Get Rusty videos.
- Practice: the first Rustlings exercises (variables, functions, if, move semantics).
- Note: compare Rust's ownership and borrowing with C++ move semantics and RAII from Quant Q27.

#### C16 · Mon 18 Jan 2027 · Rust II: structs, enums, errors
- Read and watch: Rust Book chapters 5, 6 and 9.
- Practice: Rustlings structs, enums and error handling.
- Code: a `Result`-based parser that turns order strings like "BUY 100 @ 25.5" into an `Order` struct.

#### C17 · Thu 21 Jan 2027 · Rust III: traits, generics, collections
- Read and watch: Rust Book chapters 8 and 10.
- Code `rust/order_book/`: a small order book in Rust (BTreeMap for price levels, VecDeque for the queue at each level), with unit tests. It's the same problem as Quant Q25 and Q27, so you'll be able to compare Python, C++ and Rust.

#### C18 · Mon 25 Jan 2027 · Rust IV: iterators, smart pointers, concurrency
- Read and watch: Rust Book chapters 13, 15 and 16.
- Code: a producer thread sends orders through an `std::sync::mpsc` channel to an engine thread running your C17 book. Measure the throughput, and compare it with your C++ SPSC queue from Q28.

#### C19 · Thu 28 Jan 2027 · How Solana works
- Watch: Solana Crash Course, the first chapters (roadmap, environment setup, core concepts).
- Read: the Ackee Solana Handbook on the account model, programs, rent and transactions.
- Learn: Proof of History, Sealevel parallel execution, why accounts must be declared up front, and how this differs from Ethereum.
- Setup: install the Solana CLI and Anchor (or use Solana Playground), create a devnet wallet, and airdrop devnet SOL.

#### C20 · Mon 1 Feb 2027 · Your first Anchor program
- Watch and build: the Crash Course chapters on writing and deploying an Anchor program.
- Code: a counter program (initialize, increment) deployed to devnet, with a TypeScript test.

#### C21 · Thu 4 Feb 2027 · PDAs, CPIs and SPL tokens
- Watch and build: the Developer Bootcamp project chapters on PDAs and tokens.
- Code: create an SPL token on devnet, mint to your wallet, and write a program that uses a PDA to hold tokens in a vault.

#### C22 · Mon 8 Feb 2027 · Clients and reading the chain
- Build: a client (TypeScript with the Solana web3/kit libraries, or Python) that reads your program's accounts, sends a transaction, and decodes the result.
- Practice: look up your devnet transactions on a Solana explorer and match each instruction with your code.

#### C23 · Thu 11 Feb 2027 · Solana program security
- Work through: the Solana Program Security course, covering signer authorization, owner checks, account data matching, reinitialization, PDA sharing and arbitrary CPI.
- Practice: for 3 of the attacks, write the vulnerable version and then the fixed version in Anchor.

#### C24 · Mon 15 Feb 2027 · CHECKPOINT 3: Escrow program
Deliverable `solana/escrow/` plus `reports/cp3_escrow.md`:
1. An Anchor escrow: Alice deposits token A, and Bob completes the trade by sending token B. Include cancel and refund.
2. Tests for the happy path and at least 3 attack attempts (wrong signer, wrong mint, double withdraw).
3. A security self-review against the C23 checklist.
4. Optional: apply to the next season of Ackee's School of Solana with this project.

Report back: the repo link, test output, and your self-review.

### Block D · Trading, data, other chains, custody

#### C25 · Thu 18 Feb 2027 · Market and on-chain data
- Code: use `ccxt` to download 2 years of daily candles and one day of 1-minute candles for BTC, ETH and SOL, plus perpetual funding rate history, all from public endpoints.
- Dune: fork a public dashboard on exchange flows or stablecoin supply, and edit one SQL query yourself.

#### C26 · Mon 22 Feb 2027 · Crypto as an asset: volatility, correlation, carry
- Code: rolling volatility and correlation of BTC with Nasdaq and Nifty; funding rate carry (the return from being short perp and long spot); and a simple trend rule on BTC and ETH with realistic costs. This uses your backtester from Quant Q20.
- Reflect: compare what you find with Benjamin Cowen's cycle views, noting where the data agrees with him and where it doesn't.

#### C27 · Thu 25 Feb 2027 · Crypto market making
- Work through: hftbacktest's market making tutorials on Binance futures data (basic market making, then the order book imbalance tutorial).
- Learn: perp mechanics (mark price, insurance fund, auto-deleveraging) and how liquidation cascades happen.
- Compare: your results with the Avellaneda-Stoikov simulation from Quant Q26.

#### C28 · Mon 1 Mar 2027 · Other chains, scaling and bridges
- Read: ethereum.org's developer docs on scaling (rollups) and bridges, plus any Berkeley DeFi lecture on cross-chain topics.
- Learn: optimistic vs ZK rollups (Arbitrum, Optimism, Base, zkSync), why bridges have been the biggest source of hacks, Cosmos and IBC, and Move-based chains (Aptos, Sui).
- Write: a one-page table comparing Bitcoin, Ethereum, Solana, an L2, and one Move chain on consensus, throughput, fees, programming language, and the main risk.

#### C29 · Thu 4 Mar 2027 · Custody deep dive: HD wallets, multisig, MPC
- Learn: BIP-32, BIP-39 and BIP-44 (how one seed phrase produces many keys), multisig (m-of-n scripts), MPC/TSS (one key split across parties, never put together), key ceremonies, and policy engines.
- Code: generate a BIP-39 mnemonic, derive keys along a BIP-44 path with a library, and build a 2-of-3 multisig address on Bitcoin testnet.
- By this point you'll be two months into BitGo, so compare what you build here with how BitGo's wallets work, and take your questions to your team.

#### C30 · Mon 8 Mar 2027 · CHECKPOINT 4 (capstone): Pick one
Choose one, build it, and write `reports/cp4_capstone.md`:
- (a) On-chain analytics: a Dune dashboard plus a Python notebook on stablecoin supply vs BTC price, or exchange flows vs volatility.
- (b) Full Solana dApp: your escrow plus a small web or CLI client, deployed on devnet.
- (c) Crypto strategy report: a funding-carry or trend strategy on BTC, ETH and SOL, with costs and walk-forward testing (a tear sheet like Quant CP4).

Report back: the deliverable, plus what you'd build next if you had a month.

---

## 4. Going deeper after session 30

| Interest | Next step | Free resource |
|---|---|---|
| Solana engineering | Production programs, performance, auditing | Ackee School of Solana; Ackee's free Solana Auditors Bootcamp; the Solana Bootcamp's later projects |
| Ethereum security | Auditing as a career | Cyfrin Updraft Security and Auditing course; Damn Vulnerable DeFi; CodeHawks |
| DeFi research | Mechanism design, MEV | All Berkeley DeFi lectures; Uniswap v3 and v4 docs; arXiv SoK papers |
| Crypto quant | Market making, funding arbitrage | hftbacktest advanced tutorials; Quant track Block E |
| Custody (BitGo) | Threshold cryptography | BitGo's public developer docs; MPC papers referenced there |

---

## 5. Activity log (send to me at each checkpoint)

| Checkpoint | Date | What I built | What broke | Open question |
|---|---|---|---|---|
| CP1 Minichain | Mon 14 Dec 2026 | | | |
| CP2 AMM | Mon 11 Jan 2027 | | | |
| CP3 Escrow | Mon 15 Feb 2027 | | | |
| CP4 Capstone | Mon 8 Mar 2027 | | | |

---

## 6. Full rotation calendar

Codes: Q = Quant (01_quant.md), I = Investing (02_investing.md), C = Crypto (03_crypto.md). Sundays are catch-up days. All 90 sessions finish on Mon 8 Mar 2027. If you miss a day, just do the next session in the rotation; the order matters more than the dates.

| Week of | Mon | Tue | Wed | Thu | Fri | Sat | Sun |
|---|---|---|---|---|---|---|---|
| 23 Nov |  | 24 Q01 | 25 I01 | 26 C01 | 27 Q02 | 28 I02 | 29 catch-up |
| 30 Nov | 30 C02 | 1 Q03 | 2 I03 | 3 C03 | 4 Q04 | 5 I04 | 6 catch-up |
| 7 Dec | 7 C04 | 8 Q05 | 9 I05 | 10 C05 | 11 Q06 | 12 I06 | 13 catch-up |
| 14 Dec | 14 C06 | 15 Q07 | 16 I07 | 17 C07 | 18 Q08 | 19 I08 | 20 catch-up |
| 21 Dec | 21 C08 | 22 Q09 | 23 I09 | 24 C09 | 25 Q10 | 26 I10 | 27 catch-up |
| 28 Dec | 28 C10 | 29 Q11 | 30 I11 | 31 C11 | 1 Q12 | 2 I12 | 3 catch-up |
| 4 Jan | 4 C12 | 5 Q13 | 6 I13 | 7 C13 | 8 Q14 | 9 I14 | 10 catch-up |
| 11 Jan | 11 C14 | 12 Q15 | 13 I15 | 14 C15 | 15 Q16 | 16 I16 | 17 catch-up |
| 18 Jan | 18 C16 | 19 Q17 | 20 I17 | 21 C17 | 22 Q18 | 23 I18 | 24 catch-up |
| 25 Jan | 25 C18 | 26 Q19 | 27 I19 | 28 C19 | 29 Q20 | 30 I20 | 31 catch-up |
| 1 Feb | 1 C20 | 2 Q21 | 3 I21 | 4 C21 | 5 Q22 | 6 I22 | 7 catch-up |
| 8 Feb | 8 C22 | 9 Q23 | 10 I23 | 11 C23 | 12 Q24 | 13 I24 | 14 catch-up |
| 15 Feb | 15 C24 | 16 Q25 | 17 I25 | 18 C25 | 19 Q26 | 20 I26 | 21 catch-up |
| 22 Feb | 22 C26 | 23 Q27 | 24 I27 | 25 C27 | 26 Q28 | 27 I28 | 28 catch-up |
| 1 Mar | 1 C28 | 2 Q29 | 3 I29 | 4 C29 | 5 Q30 | 6 I30 | 7 catch-up |
| 8 Mar | 8 C30 |  |  |  |  |  |  |
