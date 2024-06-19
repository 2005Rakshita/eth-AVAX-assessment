# Eth-AVAX-assessment
ERROR HANDLING 

In this project i simply explain the three main function used in solidity to handle the errors, the functions are as follow:
1) require(): this funciton is used to check and validate the condition before excuting the actual function.
2) assert(): this function is used to the condtion that  should never fail if the fails then the excution is halted.
3) revert():  is used to handle errors and revert the state changes. It can be used with or without an error message.
# Getting started
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g.,error handling.sol). Copy and paste the following code into the file:

       // SPDX-License-Identifier: MIT
     pragma solidity 0.8.25;
    contract error_handle{
    uint public flowerprice=100;
    uint public owner=200;
    
    function cost_check() public  {
    require(flowerprice>99,"costly flowers");
    flowerprice-=40;
    }
 
    function buyflowers() public view  {
    if(owner<100){
     revert("cannot buy flowers");
    }
    }
    
    function refund() public view {
    assert(owner>100);
      } 
      }

# Author 

Rakshita Thakur
thakurrakshita067@gmail.com

# License

This project is licensed under the MIT License - see the LICENSE.md file for details
