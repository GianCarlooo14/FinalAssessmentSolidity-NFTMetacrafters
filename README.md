# FinalAssessmentSolidity-SolidityToken

This is a Solidity program where a simple implementation of a token contract called "SolidityToken". The purpose of this contract is to allow us to create new tokens, which can be minted and burned as needed.

## Description

This Solidity contract is a basic implementation of a token contract called "SolidityToken". It allows the creation and destruction of tokens through the mint and burn functions. The contract can be used as a starting point for creating and managing tokens on the Ethereum blockchain.

## Getting Started

To run this program, we are going to use Remix, it is an online Solidity IDE. Just go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, click on the file explorer and create a new file. Save the file with a .sol extension, you can name the file any name you want. Copy and paste the following code into the file:

```Solidity
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract SolidityToken {


    string public tokenName = "GianCarlooo";
    string public tokenAbbrv = "GC";
    uint public totalSupply = 0; 

    mapping(address => uint) public balances;

    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    function burn (address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}


```

* Click the "Solidity Compiler" tab in the left-hand sidebar to compile the code. Click the "Compile SolidityToken.sol" button or just press "Ctrl + S" to compile the file. Also make sure that the compiler is set to "0.8.18"
* After compiling the code, by selecting the "Deploy & Run Transactions" tab in the left-hand sidebar, we can now deploy the contract. Click the "Deploy" button after selecting the "SolidityToken" contract from the menu.
* Once it is deployed, we can now interact with our code in the "Deployed Contracts". Click on the "SolidityToken" deployed contract, and then we can now call the the tokenName, tokenAbbrv, and totalSupply.
* For us to have a value in the totalSupply, we will going to call our function "mint". In that function we need to put an address and the value you want to put. To get an address we are going to use what Remix provide to us. After that put any amount or value you want to put.
* Same in the function "burn". We only need the address and then put the value you want to burn in our token. It also applies to the balances, all we need to enter is our address we use in "mint" and "burn" function.

## Authors

Gian Carlo R. Dumana

BSIT 2.5

8213650@ntc.edu.ph

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
