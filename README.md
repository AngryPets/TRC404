# TRC404: Next-gen Hybrid Memecoin Standard on Tron

## Introduction

TRC404 is an opinionated yet practical implementation of the [ERC404](https://github.com/Pandora-Labs-Org/erc404) standard, aimed at adding substantial value and utility to memecoins on EVM chains (like Tron) by enabling generative PFP NFT collections that are natively tied to them.

![TRC404 Banner](https://github.com/user-attachments/assets/be192c87-8b00-4854-aeab-d95f0c0cfbc9)

## Distinctions from Legacy ERC404

We recognized significant potential in the ERC404 standard to revolutionize the memecoin space by enabling memecoins to function like NFTs and vice versa.
However, we had to fix practical issues in the legacy ERC404:

- In legacy ERC404, 1 token equaled 1 NFT, resulting in token prices reaching thousands of dollars, unlike typical memecoins which often have many leading zeros (<0.0001). We addressed this by allowing deployers to specify the number of tokens per NFT, such as 10,000 tokens equaling 1 NFT, thereby increasing supply to resemble that of common memecoins.
- In the original ERC404, users could regenerate traits by transferring tokens between wallets, making it easy to farm rare items. We eliminated trait regeneration upon transfer; instead, users must sell their NFT and repurchase it from a DEX.
- Previously, if a user sold and rebought fractional NFTs (e.g., 0.1 NFT), the traits would change, resulting in a completely different NFT. We corrected this by tracking the user's last fractional item, effectively preventing the exploitation of rare traits.
- Miners could influence trait randomization during minting. We introduced verifiable randomness using onchain VRF to solve this issue.
- The dynamic NFT generation and art based on DNA presented a challenge in creating the metadata for them. We decided to set up a dedicated server for this generation, using off-chain data to complement the contract data. We use BTFS(or IPFS)  to store the off-chain data, saving the hash in the contract, which allows for a unique reference to this information.

## How It Works

1. **Token Generation**: Each token corresponds to a unique PFP NFT with specific traits.
2. **Minting and Trading**: Tokens are minted and can be traded on decentralized exchanges, providing immediate liquidity and fractional ownership.
3. **Reveal Process**: NFT traits are securely and randomly revealed using VRF, enhancing user engagement and trust.
4. **Dynamic Interaction**: Tokens can be used within the ERC404 ecosystem for various interactions and transactions, providing a rich, user-centric experience.

## Demonstrations

### Interaction Videos 🎬

These videos demonstrate the innovative interactions within the ERC404 ecosystem, highlighting how the tokens operate seamlessly on platforms like OpenSea and integrate with liquidity pools on Uniswap.

- [Interaction and Marketplace Integration](https://www.loom.com/share/d4734907d6ef468b87333252ff399935)
- [Uniswap Integration](https://www.loom.com/share/99e7f5ddd70a45f18e8baac79f5e9dbb)

### Workflow 🖼️

![TRC404 drawio](https://github.com/ordex-io/ERC404Meme/assets/81595884/abb414de-581c-4651-b57a-35bca117752d)

## Getting Started

To begin working with TRC404, follow these steps:

1. Clone this repository
2. Install dependencies: `npm install`
3. Run tests to ensure setup is correct: `npm test`
4. Dive into various facets and functionalities available in the ERC404 ecosystem.

## Credits

TRC404 is being collaboratively developed with insights and contributions from the teams at [Angry Pets](https://x.com/AngryPetsMeme) and [Ordex.io](https://x.com/ordex_io), along with significant individual contributions from: [@NanezX](https://github.com/NanezX), [@pash7ka](https://github.com/pash7ka)

We welcome contributions from the community. If you have suggestions, bug fixes, or enhancements, please submit a pull request or open an issue on GitHub. Let's build a more engaging and valuable memecoin ecosystem together!
