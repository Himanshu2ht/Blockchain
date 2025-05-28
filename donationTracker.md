```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract TopDonors {
    struct Donor {
        address donorAddress;
        uint256 amount;
    }

    Donor[3] public topDonors;

    function donate() public payable {
        require(msg.value > 0, "Donation cannot be zero");

        for (uint8 i = 0; i < 3; i++) {
            if (msg.value > topDonors[i].amount) {
                for (uint8 j = 2; j > i; j--) {
                    topDonors[j] = topDonors[j - 1];
                }
                topDonors[i] = Donor(msg.sender, msg.value);
                break;
            }
        }
    }
}
```
