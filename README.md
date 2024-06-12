# IceCream Token

IceCreamToken (ICA) is a simple token on Etherium. Users can mint and burn supply. 

## Description

It is designed to show the creation,minting and burning of tokens on the Etherium blockchain using Solidity. This contract here allows users to manage the supply of ice cream.

## Getting Started

### Installing

### Executing program
To run this program, we can use Remix, an online Solidity IDE:
a.Go to the Remix website at (https://remix.ethereum.org/)
b. Click on the next file option and create a new file and save it with a ".sol" extension 
c. copy and paste the code that is given in the assessment page, write your own code then.
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
*/

contract MyToken {

    // public variables here
       string public tokenName = "IceCream";
       string public tokenAbbrv = "ICA";
       uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint)public balances;
    // mint function
    function mint (address _address, uint _amount) public {
        totalSupply += _amount;
        balances[_address] += _amount;
    }
    // burn function
    function burn (address _address, uint _amount) public {
        if (balances[_address]>= _amount){
            totalSupply -= _amount;
            balances[_address] -= _amount;
        }
        
    }

}

d. compile the code by clicking on solidity compiler, ensure that the compiler is set as same as in your pragma solidity and then click on the compile option.
e. Go to the deploy the contract  select the token contract from the dropdown menu then you can make changes as you wish and burn and mint accordingly and click on deploy button.


## Help

Any advise for common problems or issues.
```
command to run if program contains helper info
```

## Authors

Devyanshika Pandey


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
