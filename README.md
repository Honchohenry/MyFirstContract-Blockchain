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
