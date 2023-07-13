# MyToken

The provided Solidity program represents a basic implementation of a token contract called "MyToken." This contract allows the creation and management of a custom token named "Correche" (abbreviated as "crrch") on the Ethereum blockchain.

## Description

The provided code represents a smart contract called "MyToken" written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract defines a custom token called "Correche" with the symbol "crrch".

## Getting Started

### Executing program

Open the Remix Ethereum online IDE in your web browser. You can access it at https://remix.ethereum.org.

Once you are on the Remix website, Create a new Solidity file by clicking on the "+" icon in the Remix file explorer on the left side of the screen.

Copy and paste the provided Solidity code into the newly created file in Remix.

```javascript
pragma solidity ^0.8.4;

contract MyToken {

    string public tokenName = "Correche";
    string public tokenAbbrv = "crrch";
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
Make sure that the Solidity Compiler is selected on the Remix interface. You can choose the appropriate compiler version by clicking on the "Compiler" tab in the right-hand panel and selecting a version that is compatible with your code.

Compile the contract by clicking on the "Compile" button in the Remix interface. You should see the compiler output in the right-hand panel, and any errors or warnings will be displayed if present.
Once the contract is successfully compiled, click on the "Deploy & Run Transactions" tab in the right-hand panel.

Click on the "Deploy" button to deploy the contract to the selected environment. This will create an instance of the contract on the blockchain.

After the contract is deployed, you will see the deployed contract details in the right-hand panel. You can interact with the contract using its functions and view its state variables.

To execute the functions, such as mint and burn, input the required parameters (e.g., _address and _value) and click the corresponding button to execute the function.

## Authors

Oscar Correche Jr.

@oscarispogi


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
