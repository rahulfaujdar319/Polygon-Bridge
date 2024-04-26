# Polygon-Bridge

## NFT Collection Deployment Project

This project aims to deploy an NFT collection on the Ethereum blockchain, utilizing image generation tools like DALLE 2 or Midjourney to create unique assets. Additionally, it involves storing these assets on IPFS, deploying the smart contract to the Goerli Ethereum Testnet, mapping the collection to the Polygon network for scalability, and transferring assets via the Polygon Bridge.

## Steps to Deploy the NFT Collection:

### 1. Generate NFT Images:

Use DALLE 2 or Midjourney to generate a 5-item collection of unique images for the NFTs.

### 2. Store Images on IPFS:

Upload the generated images to IPFS for decentralized storage. Pinata.cloud is recommended for this step.

### 3. Deploy Smart Contract:

Deploy an ERC721 or ERC1155 contract to the Goerli Ethereum Testnet. Ensure that the contract includes a `promptDescription` function to return the prompt used to generate the images.

### 4. Map NFT Collection to Polygon Network:

Map the deployed NFT collection to the Polygon network using the token mapper. This step is optional but aids in scalability and interoperability.

### 5. Write Hardhat Scripts:

Write Hardhat scripts to automate the minting and transfer processes:

- **Batch Minting**: Develop a script to batch mint all NFTs. ERC721A standard is recommended for optimal efficiency.
- **Batch Transfer to Polygon**: Implement a script to batch transfer all NFTs from Ethereum to Polygon Mumbai using the FxPortal Bridge.

## Usage:

1. Clone this repository.
2. Install dependencies using `npm install`.
3. Configure your environment variables for Ethereum and Polygon networks.
4. Run the Hardhat scripts to deploy the contract, mint NFTs, and transfer them to Polygon.

## Folder Structure:

- **contracts**: Contains the Solidity smart contracts for ERC721/ERC1155.
- **scripts**: Includes Hardhat scripts for deployment, minting, and transferring.
- **test**: Test cases for smart contracts.
- **README.md**: Instructions and information about the project.
- **.env.example**: Template for environment variables. Rename it to `.env` and fill in the required values.

## Dependencies:

- [Hardhat](https://hardhat.org/): Ethereum development environment for compiling, deploying, testing, and debugging smart contracts.
- [IPFS](https://ipfs.io/): Decentralized storage for storing NFT assets.
- [Polygon](https://polygon.technology/): Scalable Ethereum sidechain for faster and cheaper transactions.
- [FxPortal Bridge](https://docs.matic.network/docs/develop/ethereum-matic/pos/bridge): Bridge for transferring assets between Ethereum and Polygon networks.

## Contributing:

Contributions to improve the project are welcome! Feel free to submit issues or pull requests.

## License:

This project is licensed under the [MIT License](LICENSE).
