## Brief history of the blockchain + Ethereum + Solidity + Smart Contracts

---

## Miguel Vieira - @vieirapt
Co-Founder and CTO eSolidar

vieira@esolidar.com


@eSolidar

---
## About the Talk 

* Intro 
* Blockchain Overview
* Ethereum Overview
* Smart Contracts 
* Solidity Overview
* What is an ERC20 token
* ICO on Ethereum 
* Questions 

---
## #eSolidarDEV
#### Telegram - http://t.me/eSolidarDEV

---

### Blockchain
* Blockchain is like a public ledger of transactions
* Blockchain does not want to trust a third party to administer the ledger
* Blockchain is like Google Docs
* Blockchain is like DNA
+++

### Blockchain

Blockchain Network
![blockchain_network_flow](assets/blockchain_overviews.png)
+++

### Blockchain

#### Blockchain principle
* 1. A user wants to pay another user some bitcoins, he broadcasts a transaction to the network.
* 2. Miners add the transaction as they receive it to their current block, the one they are currently working on.
+++

### Blockchain

#### Blockchain principle
* 3. Randomly, one of the miner may win the lottery and "mine" the block (we'll get back to that).
* 4. At that moment, this new "definitive" block is broadcasted to the network and added to averyone's copy of the blockchain.
+++

### Blockchain
![Video](https://www.youtube.com/embed/6WG7D47tGb0)

---

### Ethereum 

   <div class="left">
     Ethereum Network
     <img src="https://s3-eu-west-1.amazonaws.com/www.yarilabs.com/assets/img/nodes.png" alt="Ethereum Network" height="400">
  </div>

  <div class="right">
    <p>
      “Each node of the Ethereum network hosts a blockchain database and 
      a node client capable of executing application code stored on blockchain.
      Nodes communicate through <span class="highlight">Wire protocol</span> and expose same interface but 
      can be implemented in different languages.”
    </p>
    <br>
    <p class="lowernote">
      Excerpt From: Roberto Infante. “Building Ethereum ÐApps” 
    </p>
  </div>

+++

### Ethereum
* Bitcoin like distributed ledger 
* Cryptocurrency (Ether)
* Ethereum Virtual Machine (EVM) 
* Turing complete
+++

### Ethereum
* Ethereum Blockchain
  * Contracts (code) 
  * Storage
  * Logs
  * Events

+++

### Ethereum
* Two kinds of accounts 
  * External Accounts (wallets controlled by humans)
  * Contract Accounts (controlled by code)
  * every account has a balance 
+++

### Ethereum
* Code execution costs GAS 
* Transaction is a message sent from one account to another and can have a data
  payload
  
---