# NFT Marketplace The Graph

> *This is an educational project with the purpose of acquiring hands-on experience in web3 application development using smart contracts written in Solidity.*

The NFT Marketplace project consists of 3 parts:

[Hardhat App](https://github.com/v7m/nft-marketplace-hardhat): This component is responsible for managing smart contracts and includes deployment scripts, using the popular development environment for Ethereum smart contracts.

[Next.js App](https://github.com/v7m/nft-marketplace-nextjs): This part serves as the frontend of the application and interacts with on-chain logic within the Ethereum ecosystem.

[The Graph App](https://github.com/v7m/nft-marketplace-graph): This component handles the storage and indexing of blockchain events. The Graph is a widely used indexing and querying protocol for blockchain data.

# Description:

NFT Marketplace is a cutting-edge platform designed for digital asset trading. The main features are:

- **Wallets Integration**: The platform is compatible with various web3 wallets, enabling easy access for a diverse user base.
- **Diverse NFT Support**: Users can trade various NFT types, including Basic (IPFS hosted) and Dynamic SVG (on-chain storage), catering to different preferences and needs.
- **Direct Minting and Listing**: Users can mint and list new NFTs directly within the marketplace, streamlining the process from creation to sale.
- **Flexible Trading Options**: Participants have the option to buy NFT tokens listed by others or set their own price when selling, providing a flexible and user-friendly trading experience.
- **Dynamic Pricing Control**: Easily modify your price or cancel a listing for your tokens at any time, offering sellers increased control over their sales strategy.
- **Revenue Management**: Sellers have full control over their trading earnings, which are withdrawable at any time, ensuring they have immediate access to their profits.

## Built with:
- Solidity
- OpenZeppelin
- Chainlink VRF
- Hardhat
- Ethers.js
- Next.js
- Moralis
- The Graph
- IPFS

# Getting Started

1. Clone the repository:

```
git clone https://github.com/v7m/nft-marketplace-graph
cd nft-marketplace-graph
```

2. Install Subgraph CLI:

```
yarn global add @graphprotocol/graph-cli
```

3. Create a New Subgraph in The Graph UI:

- Log into [The Graph UI](https://thegraph.com/studio/subgraph).
- Create a new Subgraph using `Ethereum Sepolia` as the network.

4. Initialize Subgraph:

```
graph init --studio nft-marketplace
```

5. Authenticate the CLI:

```
graph auth  --studio YOUR_DEPLOY_KEY_HERE
```

# Usage

1. Update your `subgraph.yaml` file:

    - Update the `address` field with your NftMarketplace Address
    - Update the `startBlock` field with the block number just before your contract was deployed (`blockNumber - 1`)

2. Build Subgraph locally:

```
graph codegen && graph build
```

-   `graph codegen`: Generates code in the `generated` folder based on your `schema.graphql`
-   `graph build`: Generates the build that will be uploaded to The Graph

3. Deploy Subgraph:

Replace `VERSION_NUMBER_HERE` with a version number like `0.0.1`.

```
graph deploy --studio nft-marketplace -l VERSION_NUMBER_HERE
```
