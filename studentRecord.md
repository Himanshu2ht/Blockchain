```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract StudentRecords {
    struct Student {
        string name;
        uint256 rollNumber;
    }

    mapping(uint256 => Student) private students;

    function addStudent(string memory name, uint256 rollNumber) public {
        require(bytes(name).length > 0, "Name cannot be empty");
        require(students[rollNumber].rollNumber == 0, "Roll number already exists");

        students[rollNumber] = Student(name, rollNumber);
    }

    function getStudent(uint256 rollNumber) public view returns (string memory, uint256) {
        Student memory s = students[rollNumber];
        require(s.rollNumber != 0, "Student does not exist");
        return (s.name, s.rollNumber);
    }
}
```
