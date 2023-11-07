# NFT Marketplace The Graph

*The purpose of this project is to acquire hands-on experience in web3 application development.*

The NFT Marketplace project consists of 3 parts:

[Hardhat App](https://github.com/v7m/nft-marketplace-hardhat): This component is responsible for managing smart contracts and includes deployment scripts, using the popular development environment for Ethereum smart contracts.

[Next.js App](https://github.com/v7m/nft-marketplace-nextjs): This part serves as the frontend of the application and interacts with on-chain logic within the Ethereum ecosystem.

[The Graph App](https://github.com/v7m/nft-marketplace-graph): This component handles the storage and indexing of blockchain events. The Graph is a widely used indexing and querying protocol for blockchain data.

## NFT Marketplace Features:

- Compatible with various web3 wallets.
- Trade various NFT types: Basic (IPFS hosted) and Dynamic SVG (on-chain storage).
- Buy NFT tokens listed by others or set your own price when selling.
- Easily modify your price or cancel a listing for your tokens at any time.
- Users can mint and list new NFTs directly within the marketplace.
- Sellers have full control over their trading earnings, which are withdrawable at any time.

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

1. Install Subgraph CLI:

```
yarn global add @graphprotocol/graph-cli
```

2. Create a New Subgraph in The Graph UI:

- Log into [The Graph UI](https://thegraph.com/studio/subgraph).
- Create a new Subgraph using `Ethereum Sepolia`` as the network.

3. Initialize Subgraph:

```
graph init --studio nft-marketplace
```

4. Authenticate the CLI:

```
graph auth  --studio YOUR_DEPLOY_KEY_HERE
```

5. Update your `subgraph.yaml` file:

-   Update the `address` field with your NftMarketplace Address
-   Update the `startBlock` field with the block number just before your contract was deployed (`blockNumber - 1`)

6. Build Subgraph locally:

```
graph codegen && graph build
```

-   `graph codegen`: Generates code in the `generated` folder based on your `schema.graphql`
-   `graph build`: Generates the build that will be uploaded to The Graph

7. Deploy Subgraph:

Replace `VERSION_NUMBER_HERE` with a version number like `0.0.1`.

```
graph deploy --studio nft-marketplace -l VERSION_NUMBER_HERE
```
