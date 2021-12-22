pragma solidity >=0.7.0<0.9.0;

contract BankAccount {}

contract MyBank {
    string public name;

    constructor (string memory name) {
        name = name;
    } 


}


contract Bank {
    mapping (address=>uint) public account_balances;
    function transfer(uint amount, address acctToTransferTo) external {
        account_balances[msg.sender] -= amount;
        account_balances[acctToTransferTo] += amount;

}
 function withdraw (uint amount) external{

    account_balances[msg.sender] -= amount;
    payable(msg.sender).transfer(amount);
}
 

receive () external payable {

    account_balances[msg.sender] += msg.value;
}

}
