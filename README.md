# ETH PROOF: Beginner EVM Course

A beginner-friendly Ethereum Virtual Machine (EVM) course project to help you understand the basics of Solidity and smart contract development.

## Description

This project is designed to provide a hands-on experience with creating a basic Ethereum token contract, named MyToken, allows users to mint and burn tokens. It includes public variables for the token name, abbreviation , and total supply, and a mapping to keep track of balances. The mint function increases the total supply and the balance of a specified address, while the burn function decreases them.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

/*
       REQUIREMENTS
    1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
    2. Your contract will have a mapping of addresses to balances (address => uint)
    3. You will have a mint function that takes two parameters: an address and a value. 
       The function then increases the total supply by that number and increases the balance 
       of the “sender” address by that amount
    4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. 
       It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
       and from the balance of the “sender”.
    5. Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal 
       to the amount that is supposed to be burned.

contract MyToken {
    // public variables
    string public tokenName;
    string public tokenAbbrv;
    uint public totalSupply;

    // mapping variable
    mapping(address => uint) public balances;

    // constructor
    constructor() {
        tokenName = "MyToken";
        tokenAbbrv = "MTK";
        totalSupply = 0;
    }

    // mint function
    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn(address _address, uint _value) public {
        require(balances[_address] >= _value, "Insufficient balance");
        totalSupply -= _value;
        balances[_address] -= _value;
    }
}

* Clone Repository: Clone the repository containing the Solidity file onto your local machine.

* Compile Contract: Compile the Solidity smart contract using a Solidity compiler such as Hardhat or Remix.

* Deploy Contract: Deploy the compiled contract to a blockchain network. Ensure that you have a suitable Ethereum development environment set up.

* Interact with Contract: Use a tool like Remix or web3.js to interact with the deployed contract. You can mint, burn, and transfer Nectar tokens as desired.

## Help

For any assistance or queries, feel free to reach out to the contract author via [email](namansharma272004@gmail.com).

## Authors
Naman Sharma

## License
This project is licensed under the MIT License - see the LICENSE.md file for details
