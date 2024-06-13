# Create a token

This Solidity program is a simple "create a token" program that demonstrates the basic syntax and functionality of the Solidity programming language. The purpose of this program is to serve as a starting point for those who are new to Solidity and want to get a feel for how it works.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has a single function that returns the string "Hello World!". This program serves as a simple and straightforward introduction to Solidity programming, and can be used as a stepping stone for more complex projects in the future.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., creating_sol.sol). Copy and paste the following code into the file:

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract mytoken {

    // public variables here
     string public _name ="platinum";
     string public _Abbrev = "plt";
     uint public totalSupply = 0;

    // mapping variable here
       mapping(address => uint)public balances;
    // mint function
       function mintToken(address _addr,uint _value)public{
        totalSupply += 
        _value;
        balances[_addr] += _value;
       }

    // burn function
    function burnTokens(address _addr,uint _value)public{
        if(_value<=balances[_addr])
        totalSupply -= _value ;
        balances[_addr] -=_value;
    }

}


To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile mytoken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "mytoken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the mint function or burn function. Click on the "mytoken" contract in the left-hand sidebar, and then click on the mint or burn function. Finally, click on the "transact" button to execute the function and retrieve the "Total Supply".

## Authors

Ashita BAKSH
[@bakshashita011@gmail.com)]


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
