# Welcome to TON Smart Challenge #2 by TON Foundation

There are five `.fc` files in the folder:
1. [1.fc](1.fc) - First problem "Greatest common divisor"
2. [2.fc](2.fc) - Second problem "Merge hashmaps"
3. [3.fc](3.fc) - Third problem "Message validation"
4. [4.fc](4.fc) - Fourth problem "(De)Serialize to Cell"
5. [5.fc](5.fc) - Fifth problem "Address encoder"
5. [typehelpers.fc](typehelpers.fc) - Helper library

Each file has two parts:

* Comment with description of what the smart-contract should do.

* Code of smart-contract with one or more functions marked as `testable`.

The purpose of the contestants is provide code that match description. Each task is scored from 0 to 100 points depending on number of passed tests. Each get method execution is limited by 100 000 000 (hundred millions) of gas units. This limit is high enough that it only rules out infinite loops. Any practical solution, regardless how (un)optimized it is, will fit

We ask participants to not change the signature (number, order and types of arguments and result) of `testable` functions for us to be able to evaluate their submission.

## How to submit

Solutions should be submitted as zip archive which contain up to 6 files labeled `1.fc`, `2.fc`, `3.fc`, `4.fc`, `5.fc` (each file represents a corresponding task) and `participant.json`. 

Each file will be compiled with func from [main repository](https://github.com/ton-blockchain/ton/tree/master/crypto/func). 
All contestant solutions will be linked with stdlib.fc (from [ton-blochcain repository](https://github.com/ton-blockchain/ton/blob/master/crypto/smartcont/stdlib.fc)) and [typehelpers.fc](typehelpers.fc) during compilation. Contestants are welcome to use commands from those files (note that functions declared in solution should not overwrite those in stdlib and typehelpers.fc).

`participant.json` should have the following structure:
```
{
  "address" : "your-TON-wallet-address", 
  "username": "desired-username-in-public-list",
  "codeforces": "(optional)codeforces-username"
}
```

The participant can send solutions and receive the result after short evaluation delay any number of times, but not more than 5 times per hour. The best submitted solution (with highest total score over all 5 tasks sent in one archive) will be used to determine final rank.
The organizers of the competition reserve the right to publish participants solutions with usernames (decided by participants themselves) after the contest.

## How will it be checked

For each problem we have a set of test vectors which satisfy the description. 

We will automatically run those tests against the `testable` functions. 

Solution gets points for each passed test separately. Maximal score of each task - 100 points. Gas usage does not affect score.


## Docs

We recommend participant to check out https://ton.org/docs in particular "Basic concepts" and "Smart Contracts" sections. 

Additional and detailed information is available in [whitepapers](https://ton.org/docs/#/docs).

Examples of standard smart contracts can be found [here](https://github.com/newton-blockchain/ton/tree/master/crypto/smartcont).

Developer Chats - [@tondev_eng](https://t.me/tondev_eng), [@tondev](https://t.me/tondev).

FunC studying chats - [@ton_learn](https://t.me/ton_learn), [@ton_learn](https://t.me/ton_learn)

Introduction and tutorials are available can be found at https://ton.org/docs/#/func/overview

## How to compile and test

We recommend using the [toncli](https://github.com/disintar/toncli) or [ton-contract-executor](https://github.com/Naltox/ton-contract-executor) - open source tool written by community developers.

These tool allows you to work with FunC smart contracts - compile them and run local tests.

If for some reason you don't want to use the tool you can use the FunC compiler and Fift scripts [directly](https://ton.org/docs/#/smart-contracts/?id=func).

For syntax highlighting you can use [TON IDEA Plugin](https://plugins.jetbrains.com/plugin/18541-ton-development) or [Sublime Text Plugin](https://github.com/savva425/func_plugin_sublimetext3).
