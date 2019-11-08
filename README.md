# AAVE Hackathon

This is the root repo.
The frontend repo is [here](https://github.com/jordicasesnoves/AAVE_Hackaton_frontend), as we need to split the development.



Custom implementation of basic ERC20 token using OpenZeppelin library

## Prerequisites ##
Environment: Ubuntu 18.04

Check Ubuntu version by typing
`lsb_release -a`

Check Node.js and Truffle versions  by typing  
`node -v` and  `truffle version`

Check Geth version by typing.
`geth version`
Geth is the command line interface for running a full ethereum node implelented in Go.

To install Geth, run
`sudo apt-get install software-properties-common`
`sudo add-apt-repository -y ppa:ethereum/ethereum`
`sudo apt-get update`
`sudo apt-get install ethereum`

After installing, run
`geth account new` to create an account on your node
`geth --help` to check all other options

## Steps ##

#BACKEND#

1. Set up Truffle developing framework 
  -run `npm install -g truffle`
  
2. Start a new project
  -`mkdir aave`
   `cd aave`
   `truffle init`
   
3. Truffle sets up 3 directories:
   -contracts  
   -migrations (to deploy smart contracts)
   -test (mocha style tests)
   and
   -truffle.config (to configure environments, which RPC node to use)
 
 4. Write smart contract
   
 5. Set up local blockchain. Install Ganache on your machine.https://www.trufflesuite.com/ganache
 
 6. Deploy to a local blockchain
   -`truffle migrate --network development`
 
 
 7. Deploy onto kovan test network
   -geth --kovan account new (for mainnet `geth account new`)
   
   





