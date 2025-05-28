```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract SimpleAuction {
    address public highestBidder;
    uint256 public highestBid;

    function placeBid() public payable {
        require(msg.value > highestBid, "Bid is too low.");

        if (highestBid > 0) {
            payable(highestBidder).transfer(highestBid);
        }

        highestBidder = msg.sender;
        highestBid = msg.value;
    }
}
```
