# Hemi Miner Incentivized Testnet

## Install Miner
1. Download Binaries
```bash
wget https://github.com/hemilabs/heminetwork/releases/download/v0.4.3/heminetwork_v0.4.3_linux_amd64.tar.gz
```

2. Extract Binaries
```bash
tar xvf heminetwork_v0.4.3_linux_amd64.tar.gz -C hemi-miner && cd hemi-miner
```

## Wallet
1. Create tBTC wallet
```bash
./keygen -secp256k1 -json -net="testnet" > ~/popm-address.json
```

2. Get tBTC address
```bash
cat $HOME/popm-address.json
```
`pubkey_hash` is your tBTC address

3. Fund your wallet
Get tBTC faucet in [Discord](https://discord.gg/hemixyz) for your bitcoin wallet

## Start Miner
1. Create screen
```bash
screen -S hemi
```

