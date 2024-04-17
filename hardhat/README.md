# Sample Hardhat Project

This project demonstrates a basic Hardhat use case. It comes with a sample contract, a test for that contract, and a Hardhat Ignition module that deploys that contract.

Try running some of the following tasks:

```shell
npx hardhat help
npx hardhat test
REPORT_GAS=true npx hardhat test
npx hardhat node
npx hardhat ignition deploy ./ignition/modules/Lock.js
```


🔨 Building our DAO

You want to launch a DAO for holders of your NFT Collection - CryptoDevs. From the ETH that was gained through the sale of the NFTs, you have built up a treasury. The DAO now has a lot of ETH, but currently does nothing with it.

You want to allow your NFT holders to create and vote on proposals to use that ETH for purchasing other NFTs from an NFT marketplace, and speculate on price. Maybe in the future when you sell the NFT back, you split the profits among all members of the DAO.

📝 Requirements

Anyone who owns a CryptoDevs NFT can create a proposal to purchase a different NFT from an NFT marketplace

Everyone with a CryptoDevs NFT can vote for or against the active proposals

Each NFT counts as one vote for each proposal

Voters cannot vote multiple times on the same proposal with the same NFT

If majority of the voters vote in favor of the proposal by the deadline, the NFT purchase happens automatically from the marketplace

🔩 What we will make

First, we will create a basic NFT contract for the CryptoDevs collection so we have something to test with.

Second, for the DAO to be able to purchase NFTs automatically on-chain when a proposal is passed, we need to use an on-chain NFT marketplace. While there exist a lot of on-chain NFT Marketplaces such as Seaport by OpenSea - we will create our own fake little NFT Marketplace that simulates the behavior of a real one to keep things simple and not turn this into a lesson about understanding the Seaport codebase.

Third, we will write a custom smart contract for the DAO itself where proposals can be created, voted upon, and executed on-chain.

Lastly, we will build a simple website using Next.js to allow users to create and vote on proposals.

