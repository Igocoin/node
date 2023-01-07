# node
sudo apt-get update && sudo apt-get upgrade -y
sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils python3 libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-test-dev libboost-thread-dev libboost-all-dev libboost-program-options-dev libminiupnpc-dev libzmq3-dev libprotobuf-dev protobuf-compiler unzip software-properties-common cmake -y
sudo add-apt-repository ppa:bitcoin/bitcoin
sudo apt-get update && sudo apt-get install libdb4.8-dev libdb4.8++-dev -y
wget "https://dl.walletbuilders.com/download?customer=6a35df63c8924be49aa0ef29be6dc628bdcb170f97db442472&filename=igocoin-daemon-linux.tar.gz" -O igocoin-daemon-linux.tar.gz
tar -xzvf igocoin-daemon-linux.tar.gz
wget "https://dl.walletbuilders.com/download?customer=6a35df63c8924be49aa0ef29be6dc628bdcb170f97db442472&filename=igocoin-qt-linux.tar.gz" -O igocoin-qt-linux.tar.gz
tar -xzvf igocoin-qt-linux.tar.gz
sudo mv igocoind igocoin-cli igocoin-tx /usr/bin/
mkdir $HOME/.igocoin
nano $HOME/.igocoin/igocoin.conf -t
rpcuser=rpc_igocoin
rpcpassword=dR2oBQ3K1zYMZQtJFZeAerhWxaJ5Lqeq9J2
rpcallowip=127.0.0.1
listen=1
server=1
txindex=1
daemon=1
igocoind
