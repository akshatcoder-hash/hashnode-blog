---
title: "How to deploy a smart-contract on Optimisum Goerli"
datePublished: Wed Mar 29 2023 19:01:01 GMT+0000 (Coordinated Universal Time)
cuid: clfu1ymis00010aju5g0v13yy
slug: how-to-deploy-a-smart-contract-on-optimisum-goerli
tags: blockchain, ethereum, smart-contracts, thirdweb, optimism

---

If you're looking to deploy a smart contract on any EVM (Ethereum Virtual Machine) chain, you may have encountered some roadblocks. With different chains having their own unique quirks, it can be challenging to navigate the process of deployment.

Fortunately, there's a solution: thirdweb. With thirdweb, you can deploy your smart contract on any EVM chain without the hassle of dealing with chain-specific idiosyncrasies.

Here's how it works: thirdweb is a tool that abstracts away the complexities of EVM chains, providing a unified interface that simplifies the deployment process. You can use thirdweb to deploy your smart contract on chains like Ethereum, Binance Smart Chain, and Polygon with just a few simple commands.

In this blog, we'll walk you through the steps of deploying a smart contract on any EVM chain using thirdweb. Whether you're new to smart contract development or an experienced developer, we'll provide you with the information you need to get started.

## Setting up your Development Environment

Let's examine how to build a smart contract from the ground up using the thirdweb framework and then deploy it to any blockchain that is compatible with the Ethereum Virtual Machine (EVM).

Enter the following command in your terminal while in the desired directory where you want to start the project:

```bash
npx thirdweb create contract
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680113618853/f8055fb2-3fdd-4b97-854e-690976d0815d.png align="center")

A verbose message from the thirdweb framework will appear on your terminal prompt after running the aforementioned command. You will be asked to enter a name for your project in the message. Please enter your choice of name. ThirdWeb-demo will be used in this example.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680113810070/b0a2095b-b337-498b-a79e-4f046b34758b.png align="center")

Now, choose the framework you want to use to create contracts. We will go with [Hardhat](https://hardhat.org/).

Let's name this contract as 'MyContract'

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680113823014/a2469a50-fe6e-47b8-b7ed-2f48fe6385c9.png align="center")

## Writing the Smart Contract

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680114383288/8e380db1-5e0c-478b-9b87-8d9c54fd2c0d.png align="center")

**Let me give a quick walkthrough of the contract:**

This is a simple smart contract written in Solidity. The contract is named "MyContract" and it contains a private unsigned integer variable called "value". The variable is private, which means it can only be accessed within the contract itself and not by external entities.

The contract also contains two functions: "store" and "retrieve".

The "store" function takes a uint256 argument "\_value" and sets the value of "value" to the input argument. Additionally, it emits an event "ValueChanged" with the input argument as a parameter, which can be used to track and log changes to the value.

The "retrieve" function returns the current value of "value" when called. It is marked as "view" which means that it does not modify the state of the contract, and can be called without incurring any gas cost.

The contract also includes a SPDX license identifier, which is a standardized way to indicate the license that the contract is released under. In this case, it is licensed under the MIT license.

Finally, the contract specifies the Solidity version to use, which is 0.8.17 in this case. This means that the contract can be compiled using the Solidity compiler version 0.8.17 or a higher version.

## Deploying the contract 🚀

In the same directory, run

```bash
pnpm run deploy
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680115476377/916e193a-0537-460a-8546-4dcee1a9c2fd.png align="center")

1...2...3...  
Deployed!

Your code is now compiled and deployed to IPFS.

Now, you will come across a Dashboard to choose the selected network

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680115614206/fca19e73-e90d-49c6-8b63-0d1c6c4bfbb9.png align="center")

To deploy the contract, you must have some faucet in your Testnet wallet.

Select any of the networks you want to deploy on. In this case, we are going with Optimism Goerli Testnet.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680115787669/92def491-a329-4db1-8c8c-5cad69a1948e.png align="center")

Your smart contract will start to be deployed as soon as you click the "Deploy Now" button. Your Metamask wallet will pop up and ask for your approval to continue with the deployment. A second signature request will appear after you confirm that the smart contract has been successfully deployed, allowing you to add it to the thirdweb dashboard for additional management and interaction with the dashboard's features.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680115869625/98d8fb31-bd29-487b-b496-536b6aa5988f.png align="center")

## Managing your Smart Contract

This new update of Thirdweb provides more! It even allows you to manage your Smart Contract within the web app.

You can have a look at my deployed contract here - [https://thirdweb.com/optimism-goerli/0x825d3DC4C1b16e4F16C1538f45347BcC7a961174](https://thirdweb.com/optimism-goerli/0x825d3DC4C1b16e4F16C1538f45347BcC7a961174)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680116383569/df4bcd34-9124-48cb-8646-ccbcc0752501.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680116401582/90f32457-eb4d-4f33-92b3-a8e41db7af1d.png align="center")

## Conclusion

In conclusion, thirdweb provides a user-friendly and efficient platform that enables developers to deploy smart contracts on any EVM chain seamlessly. By leveraging thirdweb’s robust features and capabilities, users can easily import, deploy, and interact with smart contracts, regardless of the underlying blockchain network. With thirdweb’s intuitive interface, developers can focus on building and refining their smart contract applications, while leaving the complexities of blockchain technology to the platform. As such, thirdweb offers an accessible and reliable solution for anyone seeking to harness the potential of smart contracts on EVM chains.

This comprehensive guide aims to provide assistance to developers of all skill levels and is intended to be beneficial for a wide range of developers. Despite its length, the information provided is intended to be easily understandable and actionable for all readers.

If you found this content helpful, please consider giving it a clap and leaving any feedback for future improvements. Your suggestions and comments are greatly appreciated and will help make these articles even more valuable for you and other readers.

Be sure to follow me to receive updates on my future articles and stay informed of new content.