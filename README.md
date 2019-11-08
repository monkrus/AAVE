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

## Installation and other operations ##
To install Geth, run
`sudo apt-get install software-properties-common`,
`sudo add-apt-repository -y ppa:ethereum/ethereum`,
`sudo apt-get update`,
`sudo apt-get install ethereum`.

After installing, run
`geth account new` to create an account on your node
`geth --help` to check all other options

 Get test Ether here : https://faucet.rinkeby.io/
 Once the transaction is confirmed, you will be able to see it on 
 `https://kovan.etherscan.io/address/<your address here>`
 
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
    Check it on https://remix.ethereum.org/#optimize=false&evmVersion=null&version=soljson-v0.5.11+commit.c082d0b4.js for errors.
   
 5. Set up local blockchain. Install Ganache on your machine.https://www.trufflesuite.com/ganache
 
 6. Deploy to a local blockchain
   -`truffle migrate --network development`
    If no error was found, proceed with deploying it on Kovan testnet.
    
 
 7. Start geth.Create new Kovan account
   `geth`
   `-geth --kovan account new` (for mainnet `geth account new`)
   
 8. List your accounts
    `geth --kovan account list`

 9. At this point, we need some test ETH.
    See ## Installation and other operations ##.
    
10. Deploy contracts on Kovan.Point Geth at the kovan network.Wait for it to sync.
    `./build/bin/geth --rinkeby --rpc --rpcapi db,eth,net,web3,personal --unlock="<your address here>"`
    
11. Once it is synced, run the migration
    `truffle migrate --network kovan`
    You should be able to see the contract in the terminal, and, also, on the Kovan testnet https://kovan.etherscan.io/.
    
    
#FRONTEND#


    
 
   
   





