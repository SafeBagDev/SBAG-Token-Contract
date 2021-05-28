# SBAG Token Contract

![SafeBag Logo](https://safebag.io/SBAG-logo.png)

SBAG is a DeFi smart contract for the [SafeBag Project](https://safebag.io/) with the following characteristics:

* Name: SafeBag
* Symbol: SBAG
* Decimals: 9

### **Tokenomics:**

* Total Supply: 100 Million
* 2% Reflection
* 3% Auto Liquidity
* Whale Protection: 2%
* Liquidity Amount: 200k

The live contract can be seen on [BscScan Here](https://bscscan.com/address/0xeb6dbdb14b0045557a8587b32767ae0dace9ff73).

The contract has been audited by Solidity Finance, [which can be found here](https://solidity.finance/audits/SBAG/).

For more information about the SafeBag Project, check out [our website](https://safebag.io/) and follow us on [Twitter](https://twitter.com/SafeBagio).

--

We realize that nowadays most token "_devs_" are just copy-pasting code without even understanding what it means, here's a step-by-step to launch your own safe token.

**Please note that this code is offered as is and no support is provided by the team.**

First, you'll need:

- yarn [here](https://yarnpkg.com/)
- ganache-cli [here](https://github.com/trufflesuite/ganache-cli)
- BscScan API Key [here](https://bscscan.com/apis)
- A wallet with some BSC

Ready? let's go.

1. Clone this repo and cd to the directory

`git clone git@github.com:SafeBagDev/SBAG-Token-Contract.git && cd SBAG-Token-Contract`

2. Install dependencies

`yarn`

3. Make changes to secrets-EXAMPLE.json
4. Rename secrets-EXAMPLE.json to secrets.json
5. Make changes to SBAGToken.sol (we've added comments for you there, so you don't have to think...)

6. Compile the contract

`hardhat compile`

7. Start a local BSC node with ganache-cli

`ganache-cli -f https://bsc-dataseed.binance.org/`

8. Deploy the contract to the local network

`npx hardhat run --network ganache scripts/deploy.js`

9. Test it's working... here you'll have to think a bit.

_All good? ok._

10. Deploy your contract to the mainnet

`npx hardhat run --network mainnet scripts/deploy.js`

_(If this doesn't work, you may need to adjust gasLimit on line 22)_

11. Finally, verify your contract on BscScan

`npx hardhat verify --network mainnet DEPLOYED_CONTRACT_ADDRESS "PANCAKESWAP_ROUTER_ADDRESS"`

_Replace DEPLOYED_CONTRACT_ADDRESS with your deployed contract address and "PANCAKESWAP_ROUTER_ADDRESS" with the pancakeswap address from secrets.json it if that's what you used._

That's it, now you have your own token.

Remember with great power comes great responsibilities, yes, even if it's on the BSC blockchain.




