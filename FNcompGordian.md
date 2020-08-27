
# Comparison FN and Gordian Wallet

**A comparison of the differences and similarities of [Fully Noded](https://github.com/Fonta1n3/FullyNoded)**, **[Gordian Wallet](https://github.com/BlockchainCommons/GordianWallet-iOS)** formerly known as FN2, **[Wasabi](https://github.com/zkSNACKs/WalletWasabi)** and **[Samourai](https://github.com/Samourai-Wallet)**.

[@Fonta1n3](https://github.com/Fonta1n3), the creator of both FN and Gordian Wallet, said it pretty straightforward when the question *What’s the difference between version FN1 and FN2?* was raised the first time in 2020: <br/>

**"Gordian is a wallet, Fully Noded is a remote control for your node"**

We'll go into much more detail of the comparison by introducing other wallets to compare with: Samourai and Wasabi.

# Similarities

All wallets complement each other in some ways. The holy grail of bitcoin secure storage is multisig and not having to rely on one app/device/codebase/etc, the best of breed wallets, like the ones we benchmark, are capable of multisig and **can be independent signers for the same multisig wallet**.

## Hardware Wallet Interface
Our comparison here keeps the discussion lean about Hardware Wallets. An extensive list can be found on github [here](https://github.com/bitcoin-core/HWI)

## The in-between role of Electrum Personal Server
"Introducing Electrum Personal Server; an implementation of the Electrum server protocol which fulfills the specific need of using the Electrum UI with full node verification and privacy, but without the heavyweight server backend, for a single user. It allows the user to benefit from all of Bitcoin Core's resource-saving features like pruning, blocksonly and disabled txindex. All of Electrum's feature-richness like hardware wallet integration, multisignature wallets, offline signing, mnemonic recovery phrases and so on can still be used, but backed by the user's own full node."
Read more about it on Reddit [here](https://www.reddit.com/r/Bitcoin/comments/7w6a9k/electrum_personal_server_the_best_way_to_connect/)

# Differences and simularities matrix

| Feature / topic                  | Fully Noded                             | Gordian Wallet                       | Wasabi Wallet                           | Samourai Wallet                           | Blue Wallet   |
| ---------------------------------| ----------------------------------------| -------------------------------------| ----------------------------------------| ----------------------------------------| ----------------| 
| ***General***                        | ***owned by Fonta1n3***   | ***owned by BlockchainCommons***             |***owned by zkSNACKs***|***owned by Katana Cryptographic***   ||
| Open Source License  | [GPLv3](https://github.com/Fonta1n3/FullyNoded/blob/master/LICENSE.md)                                         | [BSD-2](https://github.com/BlockchainCommons/GordianWallet-iOS/blob/master/LICENSE)                  | [MIT](https://github.com/zkSNACKs/WalletWasabi/blob/master/LICENSE.md)                                |[Unlicense](https://github.com/Samourai-Wallet/samourai-wallet-android/blob/develop/LICENSE)     |[MIT](https://github.com/BlueWallet/BlueWallet/blob/master/LICENSE)|
| Coordinator to be trusted               | No                                     | No        |No|Yes|TBW                                               |
| Bitcoin Core Node             |  Your own                                    | Test trusted peer node       |||Via EPS your own or trusted peer| 
| ***Objective***                        | ***full access to your nodes bitcoin-cli api***   | ***Incorporate DID into FN2, ID creation, Signing & Backup***             ||| |
| Utilizes 2FA               | No                                      | Yes                                  ||| TBW                                               |
| Cloud integration               | No                                      | Icould, for atrributes, DID Documents, Virtual Credentials?                                  |||                       |
| Account xprv can be synced to icloud | No, it's stored on the local keychain (secure enclave) only                                   | Yes                                   ||| |
| Does accounting                  | No                                      | Yes, users pseudonymous              |||    |
| Signs psbt with                  | Root xprv                               | Account based xprvs                  ||| TBW                                               |
| Multisig wallet creation         | By hand using FN                        | Automated                            ||| TBW                                               |
| Uses hot wallets on your node    | Yes                                     | No                                   ||| TBW                                               |
| Developer community                  | One lead | One lead | | || 
| **Type of wallet**               | **Multi-purpose for power user**        | **Dedicated, with ease of use in mind**  |||                                                   |
| Difference                       | a remote control for your node          | a wallet                             |||                                               |
| Import                           | Anything                                | Limited                              ||| TBW                                               |
| Node wallet access               | All                                     | Only allows access to Gordian wallets    ||| TBW                                               |
| Mix or coinjoin               | No                                     | No        | TBW                                           |||
| Pricing mechanism               | Donations                                     | Donations        |Expensive to be safe|| TBW                                               |
| Central servers               | No                                     | No        |No|Yes| TBW                                               |
| Spectrum of privacy measures       | Tor V3, Unique addr                                    | Tor V3, Unique addr    |Coinjoin |Coinjoin | |TBW                                               |
| **Feature / topic**                  | **Fully Noded**                             | **Gordian Wallet**                       | **Wasabi Wallet**                           | **Samourai Wallet**                           | **Blue Wallet**  |
| ***Hardware wallet integration***     |    |          |||
| Trezor               |                                     |        ||Watch only| 
| Ledger               |                                     |        ||Watch only| 
| Keepkey               |                                     |        ||Watch only| 
| Coldcard               |                                     |        ||Watch only| 
| Bitbox               |                                     |        ||Watch only| 
| ***Node connection***     |    |          |||
| Bitcoin Core Node        | Yes              | Gordian Server  ||No|
| Electrum Personal Server (EPS)|Only via other nodes|No|||Yes|
| Nodl             |                                      |         ||| 
| Raspiblitz             |                                      |         || 
| Embassy             |                                      |         ||| 
| myNode             |                                      |         ||| 
| ***Technical***                        | ***build from source***   | ***executable***             |||
| Lightning Enabled             | Yes                          |         ||Yes| 
| Coinjoin mixing vulnerability  | n.a.|n.a.| cancels itself out if done consecutively and leaks private data| no such vulnerability present||