# MyToken

This contract provides basic functionality for creating, managing, and transferring a cryptocurrency token. It can be used as a starting point for more complex token implementations or as a simple example for learning Solidity.

## Description

This Solidity project is a basic implementation of a cryptocurrency token, that allows for the creation, management, and transfer of a digital asset, with features including token information storage, balance mapping, minting and burning functions to increase or decrease the total supply and individual account balances, and conditional checks to ensure secure and valid transactions.

## Getting Started

### Installing

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:

contract MyToken  {

    string public tokenName = "APEX";
    string public tokenAbbrv = "APX";
    uint256 public totalSupply = 0;   
     
    mapping(address => uint256) public balances; 
    
    function mint(address _address, uint256 _value) public { 
        totalSupply += _value;
        balances[_address] += _value; }
        
        function burn (address _address, uint256 _value) public { 

        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value; 
        }
    }

}

### Executing program


To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.26" (or another compatible version ), and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MYTOKEN" contract from the dropdown menu, and then click on the "Deploy" button.

* Once the contract is deployed, click the "MYTOKEN" dropdown menu to call the mint and burn functions. 
* To call the mint function, click the drop down button beside the mint button, then copy the Account(MyToken) address and paste it in the _address input box and put in a number value in the _value input field.  
* Finally, click on the "transact" button to execute the function and retrieve the totalSupply and balances. They would reveal the totalSupply and balances values.
* Repeate the same procedure to execute the burn function.
Note that burn function executes only if the balances token is greater or equal to the inputed amount.

## Contributing
If you would like to contribute to this project, feel free to fork the repository, make your changes, and submit a pull request. Contributions are welcome! 

## Authors

Dunsin Akinbo
(https://www.linkedin.com/in/oluwadunsin-akinbo-82733b23a/)


## License

This project is licensed under the MIT License 
