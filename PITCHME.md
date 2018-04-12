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
![blockchain_network_flow](assets/images/blockchain_overviews.png)
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
* Cryptocurrency (Ether - FUEL)
* Ethereum Virtual Machine (EVM) 
* Turing-Completeness
+++

### Ethereum
* Two kinds of accounts 
  * External Accounts (wallets controlled by humans - private keys)
  * Contract Accounts (controlled by code)
  * every accounts has a balance 
+++

### Ethereum
* Ethereum account contains four fields 
  * The nonce, a counter used to make sure each transaction can only be processed once
  * The account's current ether balance
  * The account's contract code, if present
  * The account's storage (empty by default)
+++

### Ethereum
* Code execution costs GAS 
* Transaction is a message sent from one account to another and can have a data
  payload
+++

### Ethereum
* Transactions
  * The recipient of the message
  * A signature identifying the sender
  * The amount of ether to transfer from the sender to the recipient
  * An optional data field
  * A STARTGAS value, representing the maximum number of computational steps the transaction execution is allowed to take
  * A GASPRICE value, representing the fee the sender pays per computational step
+++

### Ethereum
* Messages
  * The sender of the message (implicit)
  * The recipient of the message
  * The amount of ether to transfer alongside the message
  * An optional data field
  * A STARTGAS value
+++

### Ethereum
* Ethereum Blockchain
  * Contracts (code) 
  * Storage
  * Logs
  * Events
+++

### Ethereum
* Code Execution (EVM)
  * The code in Ethereum contracts is written in a low-level (bytecode) to EVM.
  * The code consists of a series of bytes, where each byte represents an operation.
  * In general, code execution is an infinite loop (Turing-Completeness)
  * ...until the end of the code is reached or an error or STOP or RETURN instruction is detected.
+++

### Ethereum
* The operations have access to three types of space in which to store data:
  * The <b>stack</b>, a last-in-first-out container to which values can be pushed and popped
  * <b>Memory</b>, an infinitely expandable byte array
  * The contract's long-term <b>storage</b>, a key/value store. Unlike stack and memory, which reset after computation ends, storage persists for the long term.
+++
  
---

## Smart Contracts 

+++

##### What are Smart Contracts?
<p class="lowernote">
  <span class="highlight">Vitalik Buterin</span> — a smart contract approach, an asset or currency is transferred into a program “and the program runs this code and at some point it automatically validates a condition and it automatically determines whether the asset should go to one person or back to the other person, or whether it should be immediately refunded to the person who sent it or some combination thereof.”In the meantime, the decentralized ledger also stores and replicates the document which gives it a certain security and immutability.
</p>

+++

### Smart Contracts 

Smart contract flow of data 
![smart_contract_flow](assets/images/smartcontract.png)
+++

### Smart Contracts 
* Contract = code (i.e. functions) + data (i.e. state) and resides on the blockchain 
* EVM is the runtime for Smart Contracts on Ethereum
* Accounts have a persistent memory area which is called storage
* Contracts can neither read nor write to any storage apart from their own
+++

### Smart Contracts 
* Contracts can call other contracts 
* 1024 max call stack depth
* Support Events
* Contracts can purge themselves from the blockchain (OPCODE selfdestruct)

---

## Solidity Programming Language
https://solidity.readthedocs.io/
+++

### Solidity 

Solidity is a contract-oriented, high-level language for implementing smart contracts. It was influenced by C++, Python and JavaScript and is designed to target the Ethereum Virtual Machine (EVM).

+++

### Solidity 

Has some contract-specific features like:
* modifier (guard) clauses
* event notifiers for listeners 
* custom global variables.
+++

### Solidity 
Hello World

```javascript
  pragma solidity ^0.4.19;

  contract HelloWorld {

  }

```
<p class="lowernote">
  <span class="highlight">version pragma</span> — declares the version of the compiler to be used 
  to avoid breaking changes introduced on future versions
</p>
+++

### Solidity 
Statically typed language 

```javascript
  contract Example {
    // This will be stored permanently in the blockchain
    uint myUnsignedInteger = 100;
    string name;
  }
```

* `uint data type` is an unsigned integer (non-negative number) 
* `int data type` is used for signed integers
* uint has 256 bits we can also have uint8, uint16, uint32 
+++

### Solidity 
More complex data types - Structs 

```javascript
  struct TokenHolder {
    uint age;
    string obs;
  }

  // Arrays
  string[5] stringArray;
  // a dynamic Array - has no fixed size, can keep growing:
  uint[] dynamicArray;
  // Public array
  TokenHolder[] public shareHolders;
```
+++

### Solidity 
Mappings and data type address 

```javascript 
  // For a financial app, storing a uint that holds the user's account balance:
  mapping (address => uint) public accountBalance;

  // Or could be used to store / lookup usernames based on userId
  mapping (uint => string) userIdToName;
```

<ul class="lowernote">
  <li> first example, the key is an address and the value is a uint</li> 
  <li> second example, the key is a uint and the value is a string</li>
</ul>

+++

### Solidity 
Function declarations 

```javascript
  uint[] scores;

  function addNewScore(string _clientId, uint _score) public {
     ... 
     _updateScores(_score);
  }

  function _updatesScores(string _clientId, uint _number) private {
    ...
    scores.push(_number) {
    ...
  }
```
+++

### Solidity 
More about functions 

<p class="lowernote">
  So in this case we could declare it as a <b>view</b> function, meaning it's only viewing the data but not modifying it: 
</p>

```javascript
function sayHello() public view returns (string) {
```

<p class="lowernote">
    Solidity also contains <b>pure</b> functions, which means you're not even accessing any data in the app. Consider the following:
</p>

```javascript
function _multiply(uint a, uint b) private pure returns (uint) {
  return a * b;
}
```

+++

```javascript
  string greeting = "Whazaaa ?";

  function sayHello() public returns (string) {
      return greeting;
  }
```
+++

### Solidity 
Function Modifiers 

```javascript
  function sayHello() public view returns (string) {

  function _multiply(uint a, uint b) private pure returns (uint) {
    return a * b;
  }

  // Functions can return many arguments, and by specifying returned arguments
  // names we don't need to explicitly return
  function increment(uint x, uint y) returns (uint x, uint y) {
      x += 1;
      y += 1;
  }
  // when a function returns multiple values we need to parallel assign 
  (x1, y1) = increment(1,2);
```
+++

### Solidity 
More on functions Modifiers

```javascript
  modifier onlyAfter(uint _time) { require (now >= _time); _; }
  modifier onlyOwner { require(msg.sender == owner) _; }

  // Append right after function declaration
  function changeOwner(newOwner) onlyAfter(someTime) onlyOwner() {
      owner = newOwner;
  }
```
+++

### Solidity 
Payable function Modifier

```javascript
  // All functions that receive ether must be marked 'payable'
  function depositEther() public payable {
      balances[msg.sender] += msg.value;
  }
```
+++

### Solidity 
Events 
<p class="lowernote">
  Events are a way for a contract to communicate that something happened 
  on the blockchain to a front-end client that is 'listening' for events 
</p>

```javascript
  // declare the event
  event IntegersAdded(uint x, uint y, uint result);

  function add(uint _x, uint _y) public returns(uint) {
      uint result = _x + _y;
      // fire an event to let the app know the function was called:
      IntegersAdded(_x, _y, result);
      return result;
  }
```
<p class="lowernote">
  A javascript implementation would look something like:
</p>

```javascript
  YourContract.IntegersAdded(function(error, result) { 
    // do something with result
  }
```
+++

### Solidity 
Inheritance
<p class="lowernote">
  One feature of Solidity that makes this more manageable is contract inheritance:
</p>

```javascript
contract Doge {
  function catchphrase() public returns (string) {
    return "So Wow CryptoDoge";
  }
}

contract BabyDoge is Doge {
  function anotherCatchphrase() public returns (string) {
    return "Such Moon BabyDoge";
  }
}
```
+++

### Solidity 
Import
<p class="lowernote">
  When you have multiple files and you want to import one file into another, Solidity uses the import keyword:
</p>

```javascript
import "./someothercontract.sol";

contract newContract is SomeOtherContract {

}
```

+++

### Solidity 
More on Function Visibility
<p class="lowernote">
  <b>Internal</b> is the same as private, except that it's also accessible to contracts that inherit from this contract.
  <b>External</b> is similar to public, except that these functions can ONLY be called outside the contract — they can't be called by other functions inside that contract.
</p>

```javascript
contract Sandwich {
  uint private sandwichesEaten = 0;

  function eat() internal {
    sandwichesEaten++;
  }
}

contract BLT is Sandwich {
  uint private baconSandwichesEaten = 0;

  function eatWithBacon() public returns (string) {
    baconSandwichesEaten++;
    // We can call this here because it's internal
    eat();
  }
}
```

+++

### Solidity 
Using an Interface
<p class="lowernote">
  In this way, your contract can <b>interact</b> with any other contract on the Ethereum blockchain, as long they expose those functions as public or external.
</p>

```javascript
contract NumberInterface {
  function getNum(address _myAddress) public view returns (uint);
}

contract MyContract {
  address NumberInterfaceAddress = 0xab38... 
  // ^ The address of the FavoriteNumber contract on Ethereum
  NumberInterface numberContract = NumberInterface(NumberInterfaceAddress);
  // Now `numberContract` is pointing to the other contract

  function someFunction() public {
    // Now we can call `getNum` from that contract:
    uint num = numberContract.getNum(msg.sender);
    // ...and do something with `num` here
  }
}
```

+++

### Solidity 
Important global variables 

```javascript
  this; // address of contract
  this.balance; // often used at end of contract life to transfer balance 
```
```javascript
  // ** msg - Current message received by the contract ** **
  msg.sender; // address of sender
  msg.value; // amount of eth sent to contract (in wei) function should be "payable"
  msg.data; // bytes, complete call data
  msg.gas; // remaining gas
```
```javascript
lastUpdated = now;
// Will return `true` if 5 minutes have passed since `updateTimestamp` was 
// called, `false` if 5 minutes have not passed
function fiveMinutesHavePassed() public view returns (bool) {
  return (now >= (lastUpdated + 5 minutes));
}
```
+++

## Important Design Notes

<ul>
  <li> 
    <span class="highlight">Obfuscation:</span> 
       All variables are publicly viewable on blockchain, so anything that is private needs to be obfuscated </li>
  <li> 
    <span class="highlight">Storage optimization:</span> 
       Writing to blockchain is expensive, as data is stored forever</li>
</ul>
+++

## Important Design Notes

<ul>
  <li> <span class="highlight">Cron Job:</span> Contracts must be manually called to handle time-based scheduling </li>
  <li> <span class="highlight">Cost of Gas:</span> the fuel Ethereum DApps run on</li>
</ul>
---