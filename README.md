# Dria Node
# How to run Dria Node

<img src="[https://www.chasm.net/og.png](https://pbs.twimg.com/profile_banners/1741850179068678144/1723531251/1500x500)" width="3500"/>


To learn more about Dria, you can go here and read about their Blog [here](https://dria.co/blog).

[Dria](https://dria.co) is a decentralized network that allows millions of AI agents to collaborate on tasks that improve AI/ML models with synthetic data.

It is being built by the [FirstBatch](https://firstbatch.xyz) team in public so anyone can contribute to it by running a node as described in the rest of this page.



## Step 1: Check whether you have the necessary applications

### Check for git 
```bash
which git
```
If the response is “git not found” then go to [Git](https://git-scm.com/downloads) for setting it up on your device.
### Check for Docker
```bash
which docker
```
If the response is “Docker not found” then go to [Docker](https://www.docker.com/products/docker-desktop/) for setting it up on your device.

## Step 2: Clone or download the node repo from GitHub

### Run below command to clone the node repo.
```bash
git clone https://github.com/firstbatchxyz/dkn-compute-node
```

## Step 3: Set up the Environment file

### First run below line to open the node folder within the terminal.
```bash
cd dkn-compute-node
```
### Then just run the command below to create a .env file by using the example file in the repo.
```bash
cp .env.example .env
```

## Step 4 : Define your private key

### Provide your Ethereum Wallet private key
Then you should replace the YOUR_PRIVATE_KEY part from the command below with your private key and run it in the terminal.
```bash
echo "DKN_WALLET_SECRET_KEY=YOUR_PRIVATE_KEY" >> .env
```

## Step 5 : Set the AI model you prefer

### Set an open-source model via Ollama or OpenAI
It is as easy as defining your OpenAI API Key you get from the OpenAI dashboard by running the command after replacing the value with your actual key. Replace YOUR_OPENAI_API_KEY to your Api Key.
```bash
echo "OPENAI_API_KEY=YOUR_OPENAI_API_KEY" >> .env
```

## Step 6 : Now, you’re ready to kickstart your node

### First, you should run below command.
```bash
chmod +x start.sh
./start.sh --help
```
Then you’ll see this in the terminal.
![1](https://raw.githubusercontent.com/mumeido/Dria-Node/main/Dria_1.PNG)

Finally, just run the below command by replacing the model name with the model you want to serve. For OpenAI models you should write the one of the model names below:
- `gpt-4o-mini #Lowest cost`
- `gpt-4o #Price_efficient`
- `gpt-3.5-turbo`
- `gpt-4-turbo`
```bash
./start.sh -m=gpt-4o-mini
```
Here is an example screenshot of kicking the node off with an OpenAI model.
![2](https://raw.githubusercontent.com/mumeido/Dria-Node/main/Dria_2.PNG)

Once you’re done setting up a node, you can fill out this form to get the Node Keeper role in our [Discord](https://discord.gg/dria)







