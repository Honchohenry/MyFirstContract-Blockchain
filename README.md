# MyFirstContracts-Blockchain
my first contract in solidity
// SPDX-License-Identifier: GPL-3.0

pragma solidity >=0.7.0 <0.9.0; 
contract MyFirstContract {
    // state variable
    string public ourstring = "Hello World";
}

# Read and write to smart contract
contract MyFirstContract {
    // state variable
    string public ourstring = "Hello World";

    function updateOurString(string memory _updateString) public {
        ourstring = _updateString;
    }
}

# Msg.Object
// SPDX-License-Identifier: GPL-3.0

pragma solidity >=0.7.0 <0.9.0;
contract ExampleMsgSender {

    address public someAddress;

    function updateSomeAddress() public {
        someAddress = msg.sender;
    }
}

# Constructor

// SPDX-License-Identifier: GPL-3.0

pragma solidity >=0.7.0 <0.9.0;
contract ExampleConstructor {

    address public myaddress;

     constructor() {
         myaddress = msg.sender;
     }
    
    // OR

    constructor(address _address) {
        myaddress= _address;
    }

    function updateMsg(address _anotherAddress) public {
        myaddress = _anotherAddress;
    }
}
