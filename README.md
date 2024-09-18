# Hemi Miner Incentivized Testnet

## Install Miner
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

- To minizme screen: `CTRL+A+D`
- To return screen `screen -r hemi`

# View your points
* Currently, the tHEMI token payout serves as an indicator that you are PoP mining correctly. As the testnet evolves, you will have additional functionalities and uses for tHEMI tokens.
* To view your tHEMI balance, you may need to add the contract address `0x4200000000000000000000000000000000000042` as a "custom token" in your metamask wallet on Hemi Testnet Network.
* You can also import your `private_key` here to check tHEMI balance: https://pop-miner.hemi.xyz/
