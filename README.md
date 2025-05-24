# Ethereum Lottery System 🎟️

This project is a simple lottery system built on the Ethereum blockchain using Solidity. The smart contract allows multiple participants to enter the lottery by sending exactly 1 Ether. A manager account can then select a random winner, who receives the entire balance.

---

## 📜 Smart Contract Features

- ✅ Participants enter by sending exactly **1 Ether**
- 🔐 Only the **manager** can view the contract balance and select the winner
- 🎰 **Random winner selection** using `keccak256` with blockchain parameters
- 💸 Winner receives the **entire contract balance**
- 🔄 Participants array is **reset** after each draw

---

## 💻 Technologies Used

- **Solidity** (Version `>=0.5.0 <0.9.0`)
- **Ethereum Blockchain**
- **Remix IDE** for testing
- **MetaMask** wallet for transactions

---

## 🧠 How It Works

1. Deploy the contract from a manager address.
2. Any address can participate by sending exactly `1 Ether`.
3. Once there are **at least 3 participants**, the manager can call `selectWinner()`.
4. The winner is selected randomly, and the balance is transferred to them.
5. The contract resets the participants list for a new round.

---

## 📝 Functions Explained

| Function         | Description                                                  |
|------------------|--------------------------------------------------------------|
| `receive()`      | Accepts 1 Ether from participants and adds them to the list. |
| `getBalance()`   | Allows the manager to view contract balance.                 |
| `random()`       | Generates a pseudo-random number.                            |
| `selectWinner()` | Picks and transfers balance to a random winner.              |

---

## ⚠️ Requirements

- Minimum 3 participants required to draw a winner.
- Only the manager (deployer) can view balance or select winner.
- Each participant must send exactly **1 Ether**.

---

## 📂 File

- `Lottery.sol` – Contains the smart contract code.

---

## 🔗 License

This project is licensed under the MIT License.

---

## 📧 Contact

For feedback or collaboration: [YourName] - [Your Email or GitHub]

