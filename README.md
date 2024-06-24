# alcruzProject-Create-a-Token
This Solidity project involves creating a contract in the Remix environment. The goal is to create a basic implementation of a token that can be minted and burned. Minting increases the total supply and the balance of a specified address, while burning decreases the total supply and the balance of a specified address, given that the address has enough tokens to burn.

## Getting Started

### Setup/Pre-conditions
There are no installations required to execute this program, you only need a web browser. It is ideal to use Remix. Navigate to the Remix website at: https://remix.ethereum.org/.

### Executing program
1. In the Remix website, create a new file by clicking on the "+" icon in the sidebar.
2. Name the file anyway you want, just make sure you use ```.sol``` file extension.
3. Copy and paste the code from ```alcruzToken.sol``` in this repository, or from the code below.
```Solidity
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public tokenName = "SUNSHINE";
    string public tokenAbbrv = "SSN";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public {
      totalSupply += _value;
      balances[_address] += _value;
    }

    // burn function
    function burn (address _address, uint _value) public {
      if(balances[_address] >= _value) {
        totalSupply -= _value;
        balances[_address] -= _value;
      }
    }

}
```
4. Compile the code by clicking on the Solidity compiler icon in the sidebar. Make sure the version is configured correctly.
5. Click the blue compile button then click the "Deploy & Run Transactions" icon in the sidebar.
6. Click on the orange "Deploy" button.
7. Collapse your deployment and you will see all the declared variables.
8. Configure the values of these variables by checking the conditions stated in the requirements comment at the beginning of the code.

## Author
Althea Louise Cruz


