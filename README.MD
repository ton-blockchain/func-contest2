# Welcome to the TON Smart Challenge #2 by the TON Foundation

There are six.fc files in the folder:
1. [1.fc](1.fc) - First task “Greatest common divisor”
2. [2.fc](2.fc) - Second task “Merge hashmaps”
3. [3.fc](3.fc) - Third task “Message validation”
4. [4.fc](4.fc) - Fourth task “(De)Serialize to Cell”
5. [5.fc](5.fc) - Fifth task “Address encoder”
6. [typehelpers.fc](typehelpers.fc) - Helper library

Each file has two parts:

* A comment with a description of what the smart contract should do.

* The code of the smart contract with one or more functions marked as `testable`.

The goal of the contestants is provide code that match the description. Each task is scored from 0 to 100 points depending on the number of passed tests. Each get method execution is limited by 100,000,000 (hundred millions) gas units. This limit is high enough that it only rules out infinite loops. Any practical solution, regardless of how (un)optimized it is, will fit.

We ask participants not to change the signature (number, order, and types of arguments and result) of `testable` functions for us to be able to evaluate their submission.

## How to submit

Tasks are expected to be submitted through [@toncontests_bot](https://t.me/toncontests_bot).

Solutions should be submitted as a zip archive that contains up to 6 files labeled `1.fc`, `2.fc`, `3.fc`, `4.fc`, `5.fc` (each file representing a corresponding task), and `participant.json`. 

Each file will be compiled with func from the [main repository](https://github.com/ton-blockchain/ton/tree/master/crypto/func). 
All solutions from the contestants will be linked with stdlib.fc (from the [ton-blochcain repository](https://github.com/ton-blockchain/ton/blob/master/crypto/smartcont/stdlib.fc)) and [typehelpers.fc](typehelpers.fc) during compilation. Contestants are welcome to use commands from those files (note that functions declared in solution should not overwrite those in stdlib and typehelpers.fc).

`participant.json` should have the following structure:
```
{
  "address" : "your-TON-wallet-address", 
  "username": "desired-username-in-public-list",
  "codeforces": "(optional)codeforces-username"
}
```

The participant can send solutions and receive the result after a short evaluation delay any number of times, but not more than five times per hour. The best solution submitted (with the highest total score of all the five tasks sent in one archive) will be used to determine the final rank. The organizers of the competition reserve the right to publish participants’ solutions with usernames (decided by participants themselves) after the contest.

## How will it be checked

For each problem, we have a set of test vectors that satisfy the description.

We will automatically run those tests against the `testable` functions. 

A solution gets points for each passed test separately. The maximum score for each task is 100 points. Gas usage does not affect the score.


## Docs

We recommend participants check out https://ton.org/docs in particular "Basic concepts" and "Smart Contracts" sections. 

Additional and detailed information is available in the [whitepapers](https://ton.org/docs/#/docs).

Examples of standard smart contracts can be found [here](https://github.com/ton-blockchain/ton/tree/master/crypto/smartcont).

Developer Chats - [@tondev_eng](https://t.me/tondev_eng), [@tondev](https://t.me/tondev).

FunC studying chat - [@ton_learn](https://t.me/ton_learn).

Introduction and tutorials are available here: https://ton.org/docs/#/func/overview

## How to compile and test

We recommend using the [toncli](https://github.com/disintar/toncli) or [ton-contract-executor](https://github.com/Naltox/ton-contract-executor) - open-source tools written by community developers.

These tools allow you to work with FunC smart contracts, compile them, and run local tests.

If for some reason you don’t want to use the tool, you can use the FunC compiler and Fift scripts [directly](https://ton.org/docs/#/smart-contracts/?id=func).

For syntax highlighting, you can use either the [TON IDEA Plugin](https://plugins.jetbrains.com/plugin/18541-ton-development) or [Sublime Text Plugin](https://github.com/savva425/func_plugin_sublimetext3).
