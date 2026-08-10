# 🏆 Defius.gold | Elite DeFi Protocol

![Network](https://img.shields.io/badge/Network-Arbitrum%20%7C%20Base%20%7C%20Polygon%20%7C%20Optimism-gold)
![Security](https://img.shields.io/badge/Security-Direct%20Contract%20Interaction-green)

Direct smart contract interaction via Remix IDE. No website wallet connection required.

---

## 📺 Video Tutorial
Watch how to compile the interface and approve USDC safely.

[![Watch the tutorial](https://img.youtube.com/vi/YdCEfMWYu6w/maxresdefault.jpg)](https://www.youtube.com/watch?v=YdCEfMWYu6w)

---

## 🚀 Quick Start (Remix IDE)

1. **Open [Remix IDE](https://remix.ethereum.org/)**
2. **Compile Interface:** Create `DefiusInterfaces.sol` and paste the code below.
3. **Connect MetaMask:** Select "Injected Provider" in the Deploy tab.
4. **Approve USDC:** Use `IERC20Minimal` to approve the Protocol Contract.
5. **Join Pool:** Use `IDefiusPool` and call `addLiquidity()`.

---

## 📍 Essential Addresses (\$1 Tier Example)
| Contract | Address |
| :--- | :--- |
| **Protocol (Spender)** | `0x64A26d1Cba97DB97FE7Bf3819cc10249d35eDb3f` |
| **Dashboard (Read)** | `0x8db6c1987cC31A0E3081C1Dc19F52d64646A6C9E` |
| **USDC (Arbitrum)** | `0xaf88d065e77c8cC2239327C5EDb3A432268e5831` |

---

## 💻 Solidity Interface
```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

interface IERC20Minimal {
    function approve(address spender, uint256 amount) external returns (bool);
    function balanceOf(address account) external view returns (uint256);
}

interface IDefiusPool {
    function addLiquidity() external;
    function withdraw() external;
}
