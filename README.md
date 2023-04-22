# FinalAssessmentSolidity-NFTMetacrafters

Simple overview of use/purpose.

## Description

An in-depth paragraph about your project and overview of use.

## Getting Started

### Installing

* How/where to download your program
* Any modifications needed to be made to files/folders

### Executing program

* How to run the program
* Step-by-step bullets
```Solidity
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract NFTMetacrafters {


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

## Authors

Gian Carlo R. Dumana

BSIT 2.5

8213650@ntc.edu.ph

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
