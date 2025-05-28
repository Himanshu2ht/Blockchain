```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract EtherSplitter {
    address payable public address1;
    address payable public address2;
    address payable public address3;

    constructor(address payable _addr1, address payable _addr2, address payable _addr3) {
        require(_addr1 != address(0) && _addr2 != address(0) && _addr3 != address(0), "Invalid address");
        address1 = _addr1;
        address2 = _addr2;
        address3 = _addr3;
    }

    function splitEther() public payable {
        require(msg.value > 0, "Must send Ether");

        uint256 share = msg.value / 3;
        address1.transfer(share);
        address2.transfer(share);
        address3.transfer(share);
    }
}
```
