# CREATING A TOKEN

This Solidity program is a program that demonstrates the creation of a token in the Solidity programming language. The purpose of this program is to create a token and store the values in the token.

## Description

This program is a contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has multiple functions for mapping variables, minting and burning values.

## Getting Started

## Executing program

## Applications
### Create Tokens
Tokens can be generated and linked to addresses in a smart contract using the mint function. When the mint function is called, new tokens are generated and assigned to specific blockchain addresses (wallets). This process increases the total number of available tokens by adding newly minted tokens to the existing pool.

#### Mint Tokens
Tokens can be added to the current token balance once they have been produced.

#### Burn Tokens
If required, we can reduce the total amount of tokens accessible by using the burn function. As a result, tokens are taken from certain addresses, reducing their supply.

### Functions used.
#### Mint function
 function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }
#### Burn function
 function burn (address _address, uint _value) public {
        if (balances[_address] >= _value){
            totalSupply -= _value;
            balances[_address] -= _value;
        }
We can use Remix to run this code, an online Solidity IDE.

```javascript
// SPDX-License-Identifier: MIT
pragma solidity >=0.8.2 <0.9.0;

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
*/

contract newToken {

    // public variables here

    string public tokenName = "NEWTOKEN";
    string public tokenAbbrev = "NTK";
    uint public totalSupply = 0;

    // mapping variable here

    mapping (address => uint) public balances;

    // mint function

    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function

    function burn (address _address, uint _value) public {
        if (balances[_address] >= _value){
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}

```

After the code has been compiled, you may proceed to deploy the contract by navigating to the "Deploy & Run Transactions" tab located in the left-hand sidebar. Select the "newToken" contract from the dropdown menu, and then click the "Deploy" button.

Upon successful deployment of the contract, you will be able to interact with it by invoking the various functions available.

## Where to execute this code?
By working with this code on "https://remix.ethereum.org/," an easy-to-use web platform designed specifically for developing and testing Ethereum smart contracts, we may efficiently compile, deploy, and administer the ImprovedToken contract.

Moreover for detailed explantion, here's an explanatory video regarding the code, "link" kindly refer to the following link for the detailed explantion.
