# Token Creation and applying functions on it.

This Solidity program is a simple Token creation program under which we are going to demonstrates the use  of variables,functions,mapping and using all this we are going to create a contract named token which will perform functions like burn the token and mint the token .

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain.Under this smart contract we are using MIT license and also defining pragma solidity version as 0.8.20. After that we are creating the contract named mytoken under which we declare two string variables named tokename="Dhruv coin" and tokenabbr as "DUC" also we are declaring a unsigned integer totalsupply and intialize it to 0,then we mapping variable address=>value as balances,afterwards we create two functions named as mint and burn mint function for incrementing the value to that particular address and burn function to decrement the given token value from that function but inside burn function we are applying a condition that current token must be greater then the burning token.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., ethbeg.sol). Copy and paste the following code into the file:

___

// SPDX-License-Identifier: MIT
pragma solidity 0.8.20;

contract MyToken {

     string public tokenname="Dhruvcoin";
     string public tokenabbr="DUC";
     uint public totalsupply=0;
    
     mapping(address=>uint) public balances;

     function mint(address _address,uint _value) public 
     {
         balances[_address]+=_value;
         totalsupply+=_value;
     }
   
     function burn(address _address, uint _value) public {
         if(balances[_address]>=_value)
         {
             totalsupply-=_value;
             balances[_address]-=_value;
         }
     }
}
                                              ____
                                              
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.20" (or another compatible version), and then click on the "Compile ethbeg.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "ethbeg.sol" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the variable name as tokenname,tokenabbr,totalsupply , mint function and burnfunction . Click on the tokename it will give Dhruvcoin ,on tokenabbr it will give DUC,on totalsupply it will give the current total token available.On clicking on mint function we can add address and token to be added to that address.On clicking on burn function we can burn tokens on given address.

## Authors

Metacrafter Chris  
[@metacraftersio](https://twitter.com/metacraftersio)


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
