# Hemi Miner Incentivized Testnet

![image](https://github.com/user-attachments/assets/996c7d95-8be3-457b-a920-270fc337c6e1)
> Hemi is a modular protocol for superior scaling, security, and interoperability, powered by Bitcoin and Ethereum.
 
#

* For non-Node participants, you can join  pilot program [here](https://points.absinthe.network/hemi/) : Use my code to Enter: `a8389da2`
* You can run miner using web browser on windows here: https://pop-miner.hemi.xyz/

## Install Miner on Linux
**1. Download Binaries**
```bash
wget https://github.com/hemilabs/heminetwork/releases/download/v0.4.3/heminetwork_v0.4.3_linux_amd64.tar.gz
```

**2. Extract Binaries**
```bash
tar -xvf heminetwork_v0.4.3_linux_amd64.tar.gz && rm heminetwork_v0.4.3_linux_amd64.tar.gz && cd heminetwork_v0.4.3_linux_amd64
```

## Wallet
**1. Create tBTC wallet**
```bash
./keygen -secp256k1 -json -net="testnet" > ~/popm-address.json
```

**2. Get tBTC address**
```bash
cat $HOME/popm-address.json
```
* Save the output
* `pubkey_hash` is your tBTC address

**3. Fund your wallet**
* Get tBTC faucet in [Discord](https://discord.gg/hemixyz) for your bitcoin wallet
* Check your txhash in explorer until it get CONFIRMED

## Start Miner
**1. Create screen**
```bash
screen -S hemi
```

**2. Replace your private key with `PRIVATE_KEY`**
```bash
echo 'export POPM_BTC_PRIVKEY=PRIVATE_KEY' >> ~/.bashrc
echo 'export POPM_STATIC_FEE=50' >> ~/.bashrc
echo 'export POPM_BFG_URL=wss://testnet.rpc.hemi.network/v1/ws/public' >> ~/.bashrc
source ~/.bashrc
```

**3. Start your node**
```bash
./popmd
```

![image](https://github.com/user-attachments/assets/76dc9867-a0b3-4d11-9baf-cd1d5a94f695)

- To minizme screen: `CTRL+A+D`
- To return screen `screen -r hemi`

# View your points
* Currently, the tHEMI token payout serves as Hemi PoP mining points. You will get tHEMI tokens for each block you min with your Hemi Pop Node
* To view your tHEMI balance, you may need to add the contract address `0x4200000000000000000000000000000000000042` as a "custom token" in your metamask wallet on Hemi Sepolia Network.
* You can also import your `private_key` here to check tHEMI balance: https://pop-miner.hemi.xyz/
* Gaining tHEMI is delayed rn, you can check later
