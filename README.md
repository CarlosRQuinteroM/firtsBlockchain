# Blockchain Implementation with Node.js

This is a simple blockchain implementation in Node.js, consisting of a `BlockChain` class and a `Block` class.

## Block Class

The `Block` class represents a block in the blockchain. Each block contains the following attributes:

- `hash`: The hash of the block.
- `height`: The height of the block in the blockchain.
- `body`: The data contained within the block.
- `time`: The timestamp of when the block was created.
- `previousBlockHash`: The hash of the previous block in the blockchain.

### Methods

- `validate()`: Validates the integrity of the block by recalculating its hash and comparing it with the stored hash.
- `getBlockData()`: Retrieves the data stored within the block.
- `toString()`: Returns a string representation of the block.

## BlockChain Class

The `BlockChain` class represents the blockchain itself. It manages a chain of `Block` instances and provides methods for adding blocks and validating the chain.

### Methods

- `initializeChain()`: Initializes the blockchain with the genesis block if it hasn't been initialized already.
- `addBlock(block)`: Adds a new block to the blockchain after validating it.
- `validateChain()`: Validates the entire blockchain by validating each block individually.
- `print()`: Logs the contents of each block in the blockchain.

## Usage

To use this blockchain implementation, follow these steps:

1. Install Node.js if you haven't already.
2. Clone this repository.
3. Navigate to the directory containing the code.
4. Install dependencies by running `npm install`.
5. Use the classes `Block` and `BlockChain` in your own Node.js application.

## Example

```javascript
const Block = require('./block.js');
const BlockChain = require('./blockChain.js');

// Create a new blockchain
const blockchain = new BlockChain();

// Add a new block to the blockchain
const data = { message: "Hello, world!" };
const block = new Block(data);
blockchain.addBlock(block);

// Validate the blockchain
blockchain.validateChain();

// Print the contents of each block
blockchain.print();
