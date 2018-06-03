
# HeliCoin development tree

HeliCoin is a PoS-based cryptocurrency.

Rpcport - 45523

HLCC is dependent upon libsecp256k1 by sipa, the sources for which can be found here:
https://github.com/bitcoin/secp256k1

Install
-------
sudo apt-get update

sudo apt-get upgrade 

sudo apt-get install nano ntp unzip git build-essential libssl-dev libdb-dev libdb++-dev libboost-all-dev libqrencode-dev 
aptitude install miniupnpc libminiupnpc-dev

sudo apt-get install libgmp3-dev

cd helicecoin
cd src
cd leveldb
chmod 755 build_detect_platform
make clean
make libleveldb.a libmemenv.a

cd ..

make -f makefile.unix

strip helicecoind

cp helicecoind /usr/local/bin

helicecoind -daemon
-----------------
rpcuser=rpc_helicecoinu
rpcpassword=password
rpcallowip=127.0.0.1
listen=1
server=1
txindex=1
daemon=1

helicecoind stop
--------------
helicecoind -daemon
-----------------
