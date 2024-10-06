# My ERC-20 Token DApp

## Overview
This is a decentralized application (DApp) for interacting with an ERC-20 token smart contract. Users can connect their wallets, view their token balances, and send tokens to other addresses.

## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
- [Instructions](#instructions)

## Features
- Connect to MetaMask wallet
- View ERC-20 token balance
- Send tokens to other addresses

## Technologies Used
- **Ethereum**: Smart contracts using Solidity
- **Hardhat**: Development environment
- **OpenZeppelin**: ERC-20 token standard
- **JavaScript**: Frontend logic
- **HTML/CSS**: User interface

## Getting Started

### Prerequisites
- Node.js installed on your machine
- Ganache for local Ethereum blockchain

### Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Roshan003/MyDApp.git
   cd MyDApp

2. **Install Dependencies**
   Navigate to your project directory and install the required npm packages:
   ```bash
   npm install

3. Start Ganache Open Ganache and create a new workspace. Note the HTTP RPC server URL, typically http://127.0.0.1:7545. This will be used to connect your DApp to the local blockchain.

4. Deploy Your Smart Contract Run the following command to deploy your ERC-20 token smart contract:
   ```bash
   npx hardhat run scripts/deploy.js --network localhost

5. Ensure that the deployment is successful and take note of the contract address that is printed in the console.

6. Update the DApp Configuration In your app.js file, update the following variables with your deployed contract address and ABI:
   ```bash
   #javascript code
   const contractAddress = "YOUR_CONTRACT_ADDRESS_HERE"; // Replace with your contract address
   const abi = YOUR_ABI_HERE; // Replace with your contract ABI

7. Configure MetaMask Open MetaMask and create or import a wallet if you haven’t done so already.

8. Click on the network dropdown and select "Custom RPC."
   Enter the Ganache HTTP RPC URL (usually http://127.0.0.1:7545) and set the Chain ID to 1337 (or whatever chain ID is shown in Ganache).
   Add an account using one of the private keys from Ganache to fund your wallet with test Ether.
   Run the DApp Open the index.html file in your web browser. If you want to run it through a local server, you can use any local server tool or package like http-server:
   ```bash
   npx http-server

9. Then, open your browser and navigate to http://localhost:8000 (or whatever port your server is running on).

10. Connect to the Wallet
    Click on the "Connect Wallet" button in your DApp.
    Approve the connection request in MetaMask.
    The connected address and token balance should display below the button.

11. Added Features
    Features
   Connect MetaMask wallet
   Mint new tokens (only accessible by the contract owner)
   Approve a spender to transfer tokens on your behalf
   Transfer tokens to another address
   View ERC-20 token balance
