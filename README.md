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
contract ExampleMsgSender {

    address public someAddress;

    function updateSomeAddress() public {
        someAddress = msg.sender;
    }
}

# Constructor
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
# Blockchain messanger implementation
contract TheBlockchainMessanger{

    uint public changeCounter; 

    address public owner;

    string public themessage;

    constructor() {
        owner = msg.sender;
    }

    function updatethemessage(string memory _newMessage) public {
        if(msg.sender == owner){
        themessage = _newMessage;
        changeCounter++;
    }
    }  
}

# Payable Modifier and Msg.Value
contract SampleContract {
    //PAYABLE AND MSG.VALUE
    string public myString = "Hello World";

    function update(string memory _newString) public payable {
        if(msg.value == 1 ether){
            myString = _newString;
        }else {
            payable(msg.sender).transfer(msg.value);
        }
    }
}
