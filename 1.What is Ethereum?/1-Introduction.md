# What is Ethereum?

## A Short Histroy Lesson

October 31,2008 
Bitcoin:A Peer-to-Peer Electronic Cash System

December 2013 Ethereum:The Ultimate Stmart Contract and Decentralized Application Platform

Vitalik didn't want to jst use bitcoin to transfer money. He wanted to figure out some way ot use these innovations to create much more advanced applicationn. That is Smart Contract.

### What is Ethereum?
![Alt text](https://raw.githubusercontent.com/Tyebile/Ethereum-and-Solidity-Guide/master/res/network.jpg)

1. Ethereum network used to store data and transfer of money and the storage of data are what aloow us to create interesting applications which is the entire goal of Ethereum
2. There are main network and test network
3. Node is a machine that is running in Ethereum. We take a node, and install some software on it. We run that software and then it connects to Ethereum network and starts becoming a part of the network overall.
4. Anyone can run a node. Each node onn the network has a full copy of the blockchain.
5. The blockchain is being like a database that a record of evey movement of money between different parties and that's also where we store data.

## Intefacing with Ethereum Network
![Alt text](https://raw.githubusercontent.com/Tyebile/Ethereum-and-Solidity-Guide/master/res/Interfacing.jpg)

1. You can think of Web3.js as being our sort of portal where our window into the Ethereum network and it's going to allow us to send monney,store data,deploy contracts or do essentially whatever we want.
2. Metamask and Mist Browser are used for consumers. We are going to be getting a trmendous amount of experience with Metamask.

## Metamask Setup

Rinkeby Test Network is where we are going to be deploying a lot of test conntracts that we write and we'll also use it for a lot of other pruposes as well.

## Ethereum Account
![Alt text](https://raw.githubusercontent.com/Tyebile/Ethereum-and-Solidity-Guide/master/res/account.jpg)

1. Account Address - It's unique identifier that can be shared with anyone in the world and it tells other people who you are that identifies your account in some fashion. You can think of it as being like an e-mail or a user name.
2. Public Key and Private Key - They are used to authorize the sending of funds from your account to other.
3. In the Ethereum world one account is used across all different networks(Main Network and Test Network)

## Receiving Ether

http://rinkeby-faucet.com/

## Why'd we wait?
![Alt text](https://raw.githubusercontent.com/Tyebile/Ethereum-and-Solidity-Guide/master/res/wait.jpg)

We had used the Web3js library to create a transacation object and send that transactionn object to the rinkby test network then we wait for the transaction to be confimred.

![Alt text](https://raw.githubusercontent.com/Tyebile/Ethereum-and-Solidity-Guide/master/res/transaction.jpg)

Now when we sent the transaction out, it went ot one very particular node(The node has an entire copy of the blockchain). Maybe there are other people inthe world who want to submit transactions as well. So there is a lots of transactions that are coming into this node as the exact same time. All those transactions into one list of transactions which we refer to as a block the node then run some validation logic on this block that validation logic is what takes time.

The validation logic is what you might have heard many times in the past when it comes to Bitcoin or Ethereum - Mining ! Mining!.

So when those transactions right here get assembled innto the block the node starts runinng some calculationns on the block and that process is referred to as mining.

[![Blockchain 101 - A Visual Demo](https://i.ytimg.com/vi/_160oMzblY8/hqdefault.jpg?sqp=-oaymwEXCNACELwBSFryq4qpAwkIARUAAIhCGAE=&rs=AOn4CLDFXF4TIRjsoFpo5ZRo71oKHDd4qQ)](https://www.youtube.com/watch?v=_160oMzblY8)

## Smart Contracts

Smart Conntract - An account controller by code

![Alt text](https://raw.githubusercontent.com/Tyebile/Ethereum-and-Solidity-Guide/master/res/contract_account.jpg)

1. Balance Same as rur accounts have balances as well.
2. Storage can be numbers, strings, arrays any type of data that is relevant to the application
3. The code that we write on inside of our code editors are going to be compiled down to this raw machine code and it's stored inside the contract account.

So the contract account always has a good idea of exactly what it's supposed to do because it's code and instructions are stored along whit it.

![Alt text](https://raw.githubusercontent.com/Tyebile/Ethereum-and-Solidity-Guide/master/res/different_from_account.jpg)

There is ont last very critical difference between an account that we created by Metamask and a contract account. We refer to as external account, External account can use the same exact account to connnect to the all kinds of network Roberston kocan or rinkby, On the other hand theres contract account are onnly specific to onne individual network.

![Alt text](https://raw.githubusercontent.com/Tyebile/Ethereum-and-Solidity-Guide/master/res/contract_source.jpg)

Contract Source is the actual code that instructs the contract how it should behave and how it should handle monney. We will then take that contract code and deploy it to a network like say Rinekby. When we deploy this conntract code it creates an instance of the conntract or what we refer as the contract account. We can take one contract source code or one contract file and deploy multiple time to one network or multiple networks. It's very very similer to a Java Class.

## The Solidity Programming Language

![Alt text](https://raw.githubusercontent.com/Tyebile/Ethereum-and-Solidity-Guide/master/res/solidity.jpg)

Solidity is written into .sol files. Solidity is strongly typed unlike javascript which is dynamically typed. It's being similar to javascript.

![Alt text](https://raw.githubusercontent.com/Tyebile/Ethereum-and-Solidity-Guide/master/res/definition.jpg)

When we write a contract we're going to write what we called a contract definition using solidity. Solidity is acuual programming language that is very easy for you to read and interact with and understand. But it's nnot the actual code that is actually executed on the Ethereum Network inside of these Smart Contracts. Instead we're going to take that contract definition and feed it into a solidity compiler. This compiler is going to spit out two separate files.The first ont is going to contain some byte code and this actual byte code that will be deployed to the Ethereum network. On the other hand the solidity compiler is also going to spit out somethinng called the applicationn binary interface which we are going to refer to as the ABI.