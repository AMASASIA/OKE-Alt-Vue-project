
OKE_ATOMIC_MUMBAI_VUE_PROJECT


contracts/

AtomicMint.sol（NFT+SBT　”Atomic”Mint）

TBAFactory.sol（ERC-6551　Account生成）

SBT.sol（ERC-5192準拠）

Hardhat　project　　estcode

src/

App.vue（全体UI）

components/WalletButton.vue

components/AtomicMint.vue

components/OKECard.vue

firebase/

firebase.json

functions/index.js（Google AI Studio←API）

その他

README.md（Japanese/English）

.env.local.example / .env.secret.example

package.json（依存関係）


OKE_ATOMIC_MUMBAI_VUE_PROJECT/
 ├─ contracts/
 │   ├─ AtomicMint.sol
 │   ├─ TBAFactory.sol
 │   └─ SBT.sol
 │   └─ hardhat.config.js
 │   └─ test/
 │       └─ atomicMint.test.js
 ├─ src/
 │   ├─ App.vue
 │   ├─ main.js
 │   └─ components/
 │       ├─ WalletButton.vue
 │       ├─ AtomicMint.vue
 │       └─ OKECard.vue
 ├─ firebase/
 │   ├─ firebase.json
 │   └─ functions/index.js
 ├─ package.json
 ├─ .gitignore
 ├─ README.md
 └─ .env.local.example







contracts/（AtomicMint.sol, TBAFactory.sol, SBT.sol, Hardhat設定+テスト）

src/（App.vue, main.js, WalletButton.vue, AtomicMint.vue, OKECard.vue）

firebase/（firebase.json, functions/index.js）

package.json, .gitignore, .env.local.example

README.md（日英、セットアップ〜デプロイ手順のみ記載）


1. contracts/

AtomicMint.sol

ERC721 (NFT) + ERC5192 (SBT) を同時発行（Atomic Mint）

Mint 時に ERC6551 TBA を生成・紐付け

TBAFactory.sol

ERC6551 アカウント作成用のファクトリー

SBT.sol

譲渡不可の Soulbound Token（ERC-5192 準拠）

Hardhat 構成 & テスト

hardhat.config.js（Mumbai RPC 設定）

test/atomicMint.test.js（基本テスト）

2. src/

App.vue：全体 UI

main.js：エントリーポイント

components/

WalletButton.vue → MetaMask & WalletConnect v2 両対応

AtomicMint.vue → NFT+SBT 同時発行ボタン & 結果表示

OKECard.vue → NFT/SBT/TBA ステータスを表示するカード

3. firebase/

firebase.json → Hosting + Functions rewrite

functions/index.js → Google AI Studio API 呼び出し

4. その他

package.json（Vue+Vite, ethers.js, WalletConnect v2, firebase-admin）

.gitignore（node_modules, dist, .env*）

.env.local.example（Mumbai RPC, Private key, Firebase Config）

README.md（日英併記、セットアップ〜デプロイ手順のみ記載）




# OKE Atomic Mumbai Vue Project

## Setup
```bash
npm install
```

## Run locally
```bash
npm run dev
```

## Deploy Contracts (Hardhat)
```bash
npx hardhat run scripts/deploy.js --network mumbai
```

## Firebase Deploy
```bash
firebase deploy
```

### Environment Variables
See `.env.local.example`.
