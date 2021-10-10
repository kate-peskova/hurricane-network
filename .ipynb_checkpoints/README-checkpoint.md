# hurricane-network
Setting up Hurricane blockchain test network

## Hurricane Network

In this project, we will create a blockchain on a test network from scratch. This blockchain will use Proof of Authority consensus.
Throughout the project, we will use a number of private and public keys. Please note, this is a fictitious network, created for testing and study purposes only. This network’s assets carry no monetary value. Thus, private keys are allowed to be shared. However, should you create a real prototype of this network, NEVER share any of the private mainnet keys, passwords, mnemonic phrases, etc.

**Preparing the tools**.  To kick things off, we would need to upload the blockchain tools. For this project, we would use the Go Etherium (Geth) tools, which can be found through this [link](https://geth.ethereum.org/downloads/). My operating system is Mac with M1 chip. Thus, I am choosing the version “Geth & Tools 1.9.7”. Once the packet is uploaded, unzip it and rename the folder as *Blockchain-Tools*. We will get back to these tools later.

**Creating MyCrypto hot wallet**. To create our brand-new network, we need a crypto wallet address. We would fetch the addresses after we create our nodes (this step will be explained further down). To be able to access our wallets through the UI, we would need to download and istall [MyCrypto](https://download.mycrypto.com/) app.

**Creating the node directories.** Once we are all set up with the tools, we can start building our blockchain. In order to do this, we would first create the node directories using “geth” command and create new wallet addresses within them.

1. To create the first node, type in the following command:
```
./geth account new --datadir node1
```
We may use the password for enhanced security.

![](Screenshots/node1.png)

Once the command is complete, make sure to backup public and private keys.

2. Repeat the process to create node2 replacing the node1 to node2 in the prompt:
```
./geth account new --datadir node2
```
![](Screenshots/node2.png)

**Creating the Genesis Block.** Now let’s create our genesis block in our soon-to-be blockchain.
1. Navigate to the Blockchain-Tools directory inside our project and type the command `./puppeth` .

![](Screenshots/genesis1.png)

2.	Create a new network by typing its name as a command. In this project, we are creating the Hurricane network.
<genesis screen2> 
3.	In the wizard, we pick 2 to “Configure new genesis”
<genesis screen3>
4.	Then pick 1 to “Create new genesis from scratch”
<genesis screen4>
5.	Since we are creating Proof of Authority network, we would pick 2 in the next prompt and choose the default 15-second timeframe for the block by hitting enter
<genesis screen5>
6.	Now, let’s get back to our wallet addresses withing the nodes and copy them to seal the accounts (leave out 0x part)
<genesis screen6>
<genesis screen7>
