# NFT-flow
This Cadence program implements the Non-Fungible Token standard for creating and managing NFTs. This program allows users to mint new NFTs, deposit and withdraw NFTs, and transfer ownership of NFTs between users.

## Description
These files a Cadence contract that demonstrates the creation and management of non-fungible tokens (NFTs) using the standard NonFungibleToken library in the Flow blockchain. The contract allows for the creation of NFTs with metadata such as name, favorite food, and favourite Number. It also includes functions for depositing, withdrawing, transferring, and borrowing NFTs with a given ID. The CryptoPoops contract implements the NonFungibleToken standard and defines a resource called NFT for the creation of NFTs with custom metadata. It also defines a Collection resource that allows for the management of a collection of NFTs owned by a given address. The contract also includes a Minter resource for the creation of NFTs and minting them into a Collection.

The MyCollectionPublic interface defines the public functions that can be used to interact with the Collection resource, such as deposit, getIDs, borrowNFT, borrowAuthNFT, and withdraw. The createEmptyCollection function allows for the creation of an empty Collection, and the createMinter function allows for the creation of a Minter resource for minting NFTs.

The contract emits events for the initialization of the contract, as well as for the deposit and withdrawal of NFTs. Overall, this contract provides a simple implementation of NFTs and demonstrates the core functionality required for creating and managing them in a blockchain environment.

## Getting Started
### Executing program
#### Requirements
Access to a Flow network node.
Cadence Compiler
Cadence REPL
Cadence SDK
### Deploy the contract
Compile the contract using the Cadence Compiler.
Deploy the contracts "NFTCore.cdc" and "NonFungibleToken.cdc" to the Flow network node.(NOTE: deploying address should be updated on all required .cdc files)
Create the collection with "createCollection.cdc"
Mint a new NFT with "Deposit NFT.cdc"
Use Scripts to display metadata of the NFT's
### Other Usable Functions Inside The Contract
##### Withdraw an NFT
Call the getIDs() function on the Collection instance to get the list of NFT IDs you own. Call the withdraw(withdrawID) function on the Collection instance and pass in the ID of the NFT you want to withdraw. The NFT will be transferred back to the caller.

##### Transfer an NFT
Call the borrowAuthNFT(id) function on the Collection instance and pass in the ID of the NFT you want to transfer. Create a new instance of the Collection resource using the createEmptyCollection() function. Call the deposit(token) function on the new Collection instance and pass in the borrowed NFT. The NFT ownership will be transferred to the new Collection instance.

### Reading NFT metadata
The following functions can be used to read NFT metadata:

getIDs(): Returns the list of NFT IDs you own.
borrowNFT(id): Returns a borrowed reference to an NFT by ID.
borrowAuthNFT(id): Returns an authenticated borrowed reference to an NFT by ID.
The NFT resource defines the following fields:

id: The unique identifier of the NFT.
name: The name of the NFT.
favouriteDrink: The favourite Drink of the NFT.
favouriteNumber: The favourite Number of the NFT.
# Authors
Metacrafter Jacob Tucker @metacraftersio

LohithakshanMp [Blockchain developer]

License
This NFT program is not licensed.
