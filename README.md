# 🚀 Decentralized-Drive – Decentralized File Storage App

This is a decentralized alternative to traditional cloud storage solutions like Google Drive. It enables users to upload and share files securely on IPFS, with access control managed by smart contract.

Built using:
- **React.js** for frontend
- **Solidity** for smart contracts
- **Hardhat** for development
- **Pinata/IPFS** for decentralized file storage
- **Ethers.js** for blockchain interactions

---

## 📸 Features

- ✅ Upload images/files to IPFS via Pinata
- ✅ Store IPFS hash on-chain
- ✅ Share file access with other Ethereum addresses
- ✅ View files uploaded by self or shared with you
- ✅ Access-controlled display of files

---

## 🧱 Smart Contract Overview

Solidity contract manages:
- File hash storage
- Ownership and access permissions
- Sharing and revoking access

```solidity
function add(address user, string memory url) external;
function allow(address user) external;
function disallow(address user) external;
function display(address user) external view returns (string[] memory);
function shareAccess() public view returns (Access[] memory);
