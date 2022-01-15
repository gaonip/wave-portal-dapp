# Wave dapp built with hardhat

This is an example dapp built using hardhat and deployed on the rinkeby test network with the help of Alchemy.
There is a simple frontend UI created using `replit` and all wave logic is written in smart contracts using solidity.

To use this app write a message you wish to wave and click `wave`, this will real-time send a `wave` transaction through the Rinkeby test network.
Which you can then check using the etherscan here `https://rinkeby.etherscan.io/`.

To test the smart contract run, you need to install hardhat and run it locally first. 

```shell
npx hardhat
npx hardhat compile
npx hardhat test
npx hardhat run scripts/run.js
```

If you want to recompile and redeploy a new smart contract to the rinkeby testnet you can:

```shell
npx hardhat run scripts/deploy.js --network rinkeby
```

Now edit the newly deployed contract address to `./frontend/src/App.jsx` by updating the `contractAddress` parameter and copy all the compiled ABI code
under `./artifacts/contracts/wavePortal.sol/Waveportal.json` to `./frontend/src/utils/WavePortal.json`.

Enjoy and have fun with this app.