Due to my newbie github knowledge not knowing how to revert to previous commit...

I forked sector and just edited the SSL certs back

Please run the anti8444 script or similar scripts to block or remove the 8444 nodes
https://github.com/bithadder/sector-anti8444

Nodes list that are working with the Old SSL certs (this version)

sector show -a 58.234.32.51:5765

sector show -a 91.158.116.33:5765

sector show -a 147.135.7.137:5765

sector show -a 24.6.214.16:5765

sector show -a 81.224.235.46:5765

sector show -a 83.57.127.27:5765

sector show -a 23.159.160.33:5765



# sector-blockchain

Sector Blockchain is officially on Mainnet! Follow the instructions to download for linux or windows.

![GitHub contributors](https://img.shields.io/github/contributors/Chia-Network/chia-blockchain?logo=GitHub)

Sector is a modern cryptocurrency built from Chia, designed to be efficient, decentralized, and secure. Here are some of the features and benefits:
* [Proof of space and time](https://docs.google.com/document/d/1tmRIb7lgi4QfKkNaxuKOBHRmwbVlGL4f7EsBDr_5xZE/edit) based consensus which allows anyone to farm with commodity hardware
* Very easy to use full node and farmer GUI and cli (thousands of nodes active on mainnet)
* Simplified UTXO based transaction model, with small on-chain state
* Lisp-style Turing-complete functional [programming language](https://chialisp.com/) for money related use cases
* BLS keys and aggregate signatures (only one signature per block)
* [Pooling protocol](https://www.chia.net/2020/11/10/pools-in-chia.html) (in development) that allows farmers to have control of making blocks
* Support for light clients with fast, objective syncing
* A growing community of farmers and developers around the world

Please check out the [wiki](https://github.com/Sector-Network/sector-blockchain/wiki)
and [FAQ](https://github.com/Sector-Network/sector-blockchain/wiki/FAQ) for
information on this project.

Python 3.7+ is required. Make sure your default python version is >=3.7
by typing `python3`.

If you are behind a NAT, it can be difficult for peers outside your subnet to
reach you when they start up. You can enable
[UPnP](https://www.homenethowto.com/ports-and-nat/upnp-automatic-port-forward/)
on your router or add a NAT (for IPv4 but not IPv6) and firewall rules to allow
TCP port 5765 access to your peer.
These methods tend to be router make/model specific.

Most users should only install harvesters, farmers, plotter, full nodes, and wallets.
Building Timelords and VDFs is for sophisticated users, in most environments.
Chia Network and additional volunteers are running sufficient Timelords
for consensus.

### Installing

##Ubuntu/Debian

sudo apt-get update
sudo apt-get upgrade -y

sudo apt install git -y

git clone https://github.com/sector-network/sector-blockchain
cd sector-blockchain

sh install.sh

. ./activate

##If you would like to install the GUI (Which requires Gnome, XCFE or other interface)

sh install-gui.sh

cd sector-blockchain-gui
npm run electron&

##Windows Installer

Download the EXE https://github.com/Sector-Network/sector-blockchain/releases/tag/Window-Release
