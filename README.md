# 🩺 Patient Vitals On-Chain

<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/2e738604-eb11-4faa-97d7-1d1a78ee1ec9" />

A simple and transparent **Solidity smart contract** for recording and updating **patient vital signs** (like heart rate, temperature, and blood pressure) directly **on the blockchain**.  
This project demonstrates how healthcare data can be made more **secure, immutable, and decentralized** using blockchain technology.


## 📘 Project Description

The **Patient Vitals** smart contract allows patients to record their vital signs on-chain.  
Each patient is identified by their wallet address, which ensures **ownership**, **privacy**, and **trust** — only the patient can update their own vitals.  

It’s a beginner-friendly Solidity project designed to help developers understand how to:
- Use **structs** and **mappings** to store data
- Use **events** for logging updates
- Work with **modifiers** for access control
- Deploy smart contracts on **Celo testnet (Celo Sepolia)**

---

## ⚙️ What It Does

- Lets each user record their **heart rate**, **temperature**, and **blood pressure**.
- Keeps the most recent record of each patient’s vitals.
- Emits an **event** every time vitals are updated.
- Allows anyone to **view patient vitals**, but only the patient can **update** their own.

---

## ✨ Features

✅ **Decentralized Storage** — patient data lives on-chain.  
✅ **Self-Ownership** — only patients can update their own records.  
✅ **Transparency** — events allow anyone to track history of updates.  
✅ **Easy Integration** — can be used with web3.js or ethers.js in a frontend.  
✅ **Celo Compatible** — deployed on the Celo Sepolia test network.  

---

## 🌍 Deployed Smart Contract

**Network:** Celo Sepolia Testnet  
**Contract Address:** [`0x19f8daDd95d092fFce9E6B551b521f2aCE3d36A3`](https://celo-sepolia.blockscout.com/address/0x19f8daDd95d092fFce9E6B551b521f2aCE3d36A3)

---

## 💻 Smart Contract Code

```solidity
//paste your code
