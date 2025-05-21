```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract VotingSystem {
    mapping(address => bool) public hasVoted;
    mapping(string => uint256) public votesReceived;
    string[] public candidates;

    constructor(string[] memory _candidates) {
        candidates = _candidates;
    }

    function vote(string memory candidate) public {
        require(!hasVoted[msg.sender], "You have already voted.");
        votesReceived[candidate]++;
        hasVoted[msg.sender] = true;
    }

    function getVotes(string memory candidate) public view returns (uint256) {
        return votesReceived[candidate];
    }
}
```
