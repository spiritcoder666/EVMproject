# Creating a Token

This project demonstrates how to create a custom token on the Ethereum blockchain using Solidity, the primary programming language for smart contracts on Ethereum. The repository includes the Solidity source code, deployment scripts, and comprehensive instructions on how to set up and deploy your own token.
## Description

This project is an in-depth guide to creating a custom token on the Ethereum blockchain using Solidity. It covers the entire process from writing the Solidity code to deploying the token on the Ethereum network. The project aims to provide a clear understanding of the fundamental concepts of smart contracts and token creation, making it easier for developers to create their own tokens for various applications such as Initial Coin Offerings (ICOs), decentralized applications (dApps), and other blockchain-based projects.
## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:

```solidity
contract MyToken {

    // public variables here
    string public NameOfToken = "ROHITrobin";
    string public Abbrv = "Roro";
    uint256 public totalSupply = 0;

    // mapping variable here
    mapping(address => uint256) public accountBalances;

    // mint function
    function mintMyTokens(address reciever, uint256 quantity) public {
        totalSupply += quantity;
        accountBalances[reciever] += quantity;
    }

    // burn function
    function burnMyTokens(address reciever, uint256 quantity) public {
        if (accountBalances[reciever] >= quantity) {
        totalSupply -= quantity;
        accountBalances[reciever] -= quantity;
      }
   }
}


```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can use the deployed contract interface in Remix to call functions like transfer, balanceOf, etc.
## Authors

Rohit  
[@Rohit](https://mehtarohit322@gmail.com)


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
