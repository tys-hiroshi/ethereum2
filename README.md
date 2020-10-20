# ethereum2

prylabs


## Road map

https://ethereum.org/en/eth2/


## install

https://docs.prylabs.network/docs/install/install-with-script/

https://quantstamp.com/blog/how-to-be-an-eth-2-0-validator-on-the-topaz-testnet

```
mkdir prysm && cd prysm
curl https://raw.githubusercontent.com/prysmaticlabs/prysm/master/prysm.sh --output prysm.sh && chmod +x prysm.sh
```


What's the YOUR_ETH1_NODE_ENDPOINT

```
./prysm.sh beacon-chain --http-web3provider=<YOUR_ETH1_NODE_ENDPOINT>
```

create project in https://infura.io/dashboard/ethereum
get testnet Goerli Endpoint

```
./prysm.sh beacon-chain --http-web3provider=https://goerli.infura.io/v3/ff8fdcb713c349e8b1544fdb99fb26d0
```


install geth

https://github.com/ethereum/go-ethereum/wiki/Installation-Instructions-for-Mac

```
brew tap ethereum/ethereum
brew install ethereum
```

```
geth --goerli --datadir="$HOME/Goerli"
./prysm.sh beacon-chain --http-web3provider=$HOME/Goerli/geth.ipc
```

➜  prysm git:(main) ✗ ./prysm.sh beacon-chain --http-web3provider=$HOME/Goerli/geth.ipc
Latest Prysm version is v1.0.0-alpha.29.
Beacon chain is up to date.
gpg is not available. Either install it or run with PRYSM_ALLOW_UNVERIFIED_BINARIES=1.