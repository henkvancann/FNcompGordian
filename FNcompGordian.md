# ALWAYS UNDER CONSTRUCTION!! BECAUSE WALLETS CHANGE EVERY WEEK.
# Comparison FN and Gordian Wallet against other bitcoin-only wallets

**A comparison of the differences and similarities of [Fully Noded](https://github.com/Fonta1n3/FullyNoded)**, **[Gordian Wallet](https://github.com/BlockchainCommons/GordianWallet-iOS)** formerly known as FN2, **[Wasabi](https://github.com/zkSNACKs/WalletWasabi)**, **[Samourai](https://github.com/Samourai-Wallet)** and **[Blue Wallet](https://github.com/Bluewallet)**.

### Exoplanation of features to compare
See our [Legend](./Legend.md).

# Similarities

All wallets complement each other in some ways.

## Teamplayers Gordian Wallet (GW) and Fully Noded (FN)
The general idea is `multisig` is by far the most secure way to use bitcoin, both GW and FN are excellent multsig wallets, it’s generally a good idea to use many wallets for your multisig setup, with that in mind the two together make an excellent team.

## All 'Bitcoin only' wallets
Except for Gordian Wallet, which also keeps keys for Decentralised IDs.

## Developers (have) the same (background)
GW and FN are developed by the one and only developer `@Fonta1n3`. Wasabi and Samourai are both CoinJoin derivates. Developers of Wasabi and Samourai know eachother very well. They have their mutual background and dito rivalry.

## Hardware Wallet Interface
Our comparison here keeps the discussion lean about Hardware Wallets. An extensive list can be found on github [here](https://github.com/bitcoin-core/HWI)

## The in-between role of Electrum Personal Server
"Introducing Electrum Personal Server; an implementation of the Electrum server protocol which fulfills the specific need of using the Electrum UI with full node verification and privacy, but without the heavyweight server backend, for a single user. It allows the user to benefit from all of Bitcoin Core's resource-saving features like pruning, blocksonly and disabled txindex. All of Electrum's feature-richness like hardware wallet integration, multisignature wallets, offline signing, mnemonic recovery phrases and so on can still be used, but backed by the user's own full node."
Read more about it on Reddit [here](https://www.reddit.com/r/Bitcoin/comments/7w6a9k/electrum_personal_server_the_best_way_to_connect/)

# Differences

## "Gordian is a wallet, Fully Noded is a remote control for your node"

says [@Fonta1n3](https://github.com/Fonta1n3), the creator of both FN and Gordian Wallet, said it pretty straightforward when the question *What’s the difference between version FN1 and FN2?* was raised the first time in 2020: <br/>
We'll go into much more detail of the comparison by introducing other wallets to compare with: Samourai and Wasabi.

## Multi-signature
The holy grail of bitcoin secure storage is multisig and not having to rely on one app/device/codebase/etc, most best of breed wallets, like some wallets that we benchmark, are capable of multisig and **can be independent signers for the same multisig wallet**.
Blue Wallet, Wasabi and Samourai are not yet capable of mutli-sign (Blue Wallet says 'Coming soon' as of Aug 2020, which Samourai stated in 2018 already....)


# Differences and simularities matrix

| Feature / topic                  | Fully Noded                             | Gordian Wallet                       | Wasabi Wallet                           | Samourai Wallet                           | Blue Wallet   |
| ---------------------------------| ----------------------------------------| -------------------------------------| -----------------------------------| ----------------------------------------| ---------------------------| 
| ***General***                        | ***owned by Fonta1n3***   | ***owned by BlockchainCommons***             |***owned by zkSNACKs***|***owned by Katana Cryptographic***   |**owned by Bluewallet Services, S.R.L., 3 shareholders/developers?**|
| [Open Source License](./Legend.md#Open-Source-License)  | [GPLv3](https://github.com/Fonta1n3/FullyNoded/blob/master/LICENSE.md)                                         | [BSD-2](https://github.com/BlockchainCommons/GordianWallet-iOS/blob/master/LICENSE)                  | [MIT](https://github.com/zkSNACKs/WalletWasabi/blob/master/LICENSE.md)                                |[Unlicense](https://github.com/Samourai-Wallet/samourai-wallet-android/blob/develop/LICENSE)     |[MIT](https://github.com/BlueWallet/BlueWallet/blob/master/LICENSE)|
| [Coordinator to be trusted](./Legend.md#Coordinator-to-be-trusted)               | No                                     | No        |No|Yes|No|
| [Devices](./Legend.md#Devices)             |  Mobile  (iOS only)                                 | Mobile (iOS only)      |Desktop (Mac and Windows) |Mobile (iOS/Android)|Mobile (iOS/Android) and Desktop (Mac and Windows)nO|
| [Net available](./Legend.md#Net-available)                 | **Main**, Test, Regtest, LN | Test, Regtest | **Main**, Test, Regtest | **Main**, Test | **Main**, LN|
| ***Objective***                        | ***full access to your nodes bitcoin-cli api***   | ***Incorporate DID into FN2, ID creation, Signing & Backup***             |||**have a Bitcoin only wallet, full control of the transactions, support Segwit and fee control**|
| [Utilizes 2FA](./Legend.md#Utilizes-2FA)               | No                                      | Yes                                  |No| No                                              |No|
| [Cloud integration](./Legend.md#Cloud-integration)               | No                                      | Icould, for atrributes, DID Documents, Virtual Credentials?                                  ||*Don't mistake* Wasabi **cloud storage** for Wasabi **wallet**|No|
| [Account xprv can be synced to cloud service](./Legend.md#Account-xprv-can-be-synced-to-cloud-service) | No, it's stored on the local keychain (secure enclave) only                                   | Yes                                   |||No,but pub keys could be disclosed via EPS to peer nodes|
| [Does accounting](./Legend.md#Does-accounting)                  | No                                      | Yes, users pseudonymous              |||No|
| Feature / topic                  | Fully Noded                             | Gordian Wallet                       | Wasabi Wallet                           | Samourai Wallet                           | Blue Wallet   |
| [Buy and sell bitcoin](./Legend.md#Buy-and-sell-bitcoin)        | No                                      | No              |||Yes, p2p exchange no KYC|
| [Signs psbt with](./Legend.md#Signs-psbt-with)                  | Root xprv                               | Account based xprvs                  ||| TBW                                               |
| [Multisig wallet creation](./Legend.md#Multisig-wallet-creation)         | By hand using FN, FN never adds a private key to your node unless you manually import a `wif` or `xprv`  | Automated, creates a 2/3 multisig wallet. Your node is a signer as well as your device. Then you can keep one offline backup of a seed.          ||No| TBW                                               |
| [Uses hot wallets on your node](./Legend.md#Uses-hot-wallets-on-your-node)    | Yes                                     | No                                   |Yes|Yes| Yes                                               |
| [Decentralized identity creation]((./Legend.md#Decentralized-identity-creation))  | No                                      | Yes                                  | No| No| No|
| [Developer community](./Legend.md#Developer-community)         | One lead | One lead | | |3 developers| 
| **[Type of wallet](./Legend.md#Type-of-wallet)**               | **Multi-purpose for power user**        | **Dedicated, with ease of use in mind** |**Coinjoin**|**Coinjoin**|**Simple**|
| [Difference](./Legend.md#Difference)                    | a remote control for your node          | a wallet                             |a coin mixing privacy wallet|a coin mixing privacy wallet| a simple wallet available on many devices
| [Import](./Legend.md#Import)                        | Anything                                | Limited                              ||| TBW                                               |
| [Node wallet access](./Legend.md#Node-wallet-access)            | All                                     | Only allows access to Gordian wallets    ||| via EPS                                               |
| [Mix or coinjoin](./Legend.md#Mix-or-coinjoin)               | No                                     | No        |Yes|Yes|No|
| [Pricing mechanism](./Legend.md#Pricing-mechanism)             | Donations                                     | Donations        |Expensive to be safe|Fees on coinjoins| Donations                                         |
| [Central servers](./Legend.md#Central-servers)               | No                                     | No        |No|Yes| No                                               |
| [Spectrum of privacy measures](./Legend.md#Spectrum-of-privacy-measures)  | Tor V3, Unique addr                                    | Tor V3, Unique addr    |Coinjoin |Coinjoin |EPS|TBW                                               |
| **Feature / topic**                  | **Fully Noded**                             | **Gordian Wallet**                       | **Wasabi Wallet**                           | **Samourai Wallet**                           | **Blue Wallet**  |
| ***[Hardware wallet integration](./Legend.md#Hardware-wallet-integration)***     |    |          |||
| Trezor               | TBW                          |         |        ||Watch only| 
| Ledger               | TBW                           |     |        ||Watch only| 
| Keepkey               | TBW                           |   |        ||Watch only| 
| Coldcard               | TBW                           |   |        ||Watch only| 
| Bitbox               |  TBW                         |          |        ||Watch only|
| Cobo Vault            | TBW                          |       |        ||Watch only|  
| ***[Node connection](./Legend.md#Node-connection)***     |||||
| Bitcoin Core Node        | Yes              | Gordian Server  |Yes|Dojo|No|
| Electrum Personal Server (EPS)|Only via other nodes|No|||Yes|
| Nodl             |Yes                                      |   |      ||Yes, because EPS available| 
| Raspiblitz             |Yes                                     || |         |Yes, because EPS available| 
| Embassy             |Yes                                    |     |    ||No| 
| myNode             |Yes                                      |     |    ||No| 
| ***[Technical](./Legend.md#Technical)***                        | ***build from source***   | ***executable***             |||***build from source***|
| [Github](./Legend.md#Github)             |[Fully Noded](https://github.com/Fonta1n3/FullyNoded)** | **[Gordian Wallet](https://github.com/BlockchainCommons/GordianWallet-iOS)** | **[Wasabi](https://github.com/zkSNACKs/WalletWasabi)** | **[Samourai](https://github.com/Samourai-Wallet)** | **[Blue Wallet](https://github.com/Bluewallet)**|
| [BIP support](./Legend.md#BIP-support) | TBW | | | | |
| [Lightning Enabled](./Legend.md#Lightning-Enabled)             | Yes                          |No       |||Yes| 
| [Coinjoin mixing vulnerability](./Legend.md#Coinjoin-mixing-vulnerability)  | No|No| cancels itself out if done consecutively and leaks private data| no such vulnerability present|No|
|