# SaferMoonProtocol BSCCore
* **Objective** - To create a template for launchin cryptos

## PreRequisites
* Create Ethereum wallet
* Install Chrome, Firefox, Opera
* Install MetaMask
* Link MetaMask to Ethereum Wallet
* Create MetaMask Test Wallet
* Generate Currency From Faucet
* Install NodeJS
* Install TruffleJS
* Install Ganache

## Instructions for Creating Your Own Coin
* Execute the command below to install node packages
	* `npm install`
* Execute the command below to create a `.env` file
	* `node ./automation/create-env.js`
* Execute the command below to access truffle console
	* `truffle console --network ropsten`
* Execute the command below from the truffle console
	* `web3.eth.getAccounts()`
* Copy the first address listed
	* send ether to first account listed
* Verify the address has ether after sending it
	* `web3.eth.getBalance('0xAddressOfAccount');`
* Execute the command below from the root directory of this project
	* `./deploy-application.sh`


## Instructions for Local Deployment
* Upon cloning the project execute the command below to start a local blockchain fork
  * `./start-local-blockchain-fork.sh`
* Upon running a local blockahin fork, execute the following command from the root directory of the project to deploy a smart contract to your local Ganache.
  * `./deploy-application.sh`
* Ensure the `contracts/SaferMoonProtocolDeFi.sol` file is referring to a local-ganache token
  * `IUniswapV2Router02 _uniswapV2Router = IUniswapV2Router02(:routerAddress);`
