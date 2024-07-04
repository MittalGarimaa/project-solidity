## MyToken Smart Contract

## Introduction

The provided Solidity code represents a basic smart contract named "MyToken," designed to simulate the behavior of an ERC20-like token on the Ethereum blockchain. This contract allows the creation and destruction of tokens within a decentralized system. Through its functions, users can mint new tokens and burn existing tokens from their own balances. The contract runs on the Ethereum Virtual Machine (EVM) and adheres to Solidity version ^0.8.0.

 ## Getting Started

 ## Execution

To run this program, you can use tools like Remix IDE.

You can execute this program using Remix, a web-based Solidity IDE. To get started, visit the [Remix IDE website](https://remix.ethereum.org/).

Once you're on the Remix website, create a new file by clicking the "+" icon on the left-hand sidebar. Save the file with a `.sol` extension, for example, "MyToken.sol". Then, copy and paste the provided code into the new file.

```solidity
// SPDX-License-Identifier: UNLICENSED
pragma solidity ^0.8.0;

contract MyToken {
    // Public variables
    string public tokenName = "MyToken";
    string public tokenAbbrv = "MTK";
    uint public totalSupply = 0;

    // Mapping to track balances
    mapping(address => uint) public balances;

    // Mint function
    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // Burn function
    function burn(address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}
```

To compile the code, go to the "Solidity Compiler" tab on the left-hand sidebar. Ensure that the "Compiler" option is set to "^0.8.0", then click on the "Compile MyToken.sol" button.

After compiling the code, deploy the contract by navigating to the "Deploy & Run Transactions" tab on the left-hand sidebar. Click the "Deploy" button to deploy the contract.

Once deployed, you can use the `mint` and `burn` functions by specifying the address and the amount to be minted or burned. Additionally, you can use the `balances` mapping to check the token balance of any account by providing the address.

This project is licensed under the MIT License. 
## Authors
Garima Mittal
[@MittalGarimaa](https://github.com/MittalGarimaa)
