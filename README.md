# First-Solidity-Project


# Overview

The Solidity smart contract would meet the following requirements:

1. Token Details: Store public variables for token name, abbreviation, and total supply.
2. Balance Mapping: Map addresses to balances (address => uint).
3. Mint Function: Increase total supply and balance of a given address by a specified value.
4. Burn Function: Decrease total supply and balance of a given address by a specified value, with conditional checks to prevent overdrafts.

Requirements

- Solidity version: 0.8.18
- Public variables for token details
- Mapping of addresses to balances
- Mint function with address and value parameters
- Burn function with address and value parameters, including conditional checks

# Project Structure

MyToken.sol: The main contract file containing the implementation


## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has mint and burn functions.The mint function increases the totalSupply by the given value, while the burn function reduces the balances and total Supply of token by the given value.
This program serves as a simple and straightforward introduction to Solidity programming, and can be used as a stepping stone for more complex projects in the future.


# myToken 

contract MyToken {

    
string public tokenName = "APEX"
string public tokenAbbrv = "APX"
unit public totalSupply = 0; 


mapping(address => unit) public balances;

function mint(address_address, uint_value) public { 
 totalSupply +=  _value;
    balance[_address] += _value;}


function mint(address_address, uint_value) public {
 If ( balances[_address] >= _value)
{totalSupply -=  _value;
balances[_address] -= _value;}
}

}
## Getting Started


To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile myToken.sol" button.


Click solidity compiler icon
Ensure the compile checkbox is checked and then click Compile myToken
Then click Deply & run transaction icon below
Then click deploy(orange button)
Click the small copy button at the right under ACCOUNT
Move downwards and click the arrow button under mint, then
Paste the the copied value into the  _address input field
Then put 1000 in the _value input field and click transact.


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
