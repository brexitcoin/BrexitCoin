# **Brexit (BRXT) Version 1.1.0.0**
#Date Last Compiled : July 1st 2016 #

Brexit Integration/Staging Tree
================================
![BRXT logo](https://raw.githubusercontent.com/brexitcoin/BrexitCoin/master/src/qt/res/icons/novacoin-128.png)

**Copyright (c) 2016 The Brexit Developers**

#### What is Brexit?
----------------
* Algorithm: Scrypt
* Coin Suffix: BRXT
* PoW Period: 62016 Blocks
* PoW Target Spacing: 60 Seconds
* PoW Difficulty Retarget: 8 Blocks
* PoW Reward per Block: 1000 BRXT
* Full Confirmation: 8 Blocks
* Maturity: 16 Blocks
* PoS Target Spacing: 64 Seconds
* PoS Difficulty Retarget: 10 Blocks
* PoS Reward: 4% 
* Minimum Confirmations for Stake: 16 Blocks
* PoS Min: 4 Hour
* PoS Max: Unlimited
* Total Coins: 494,117,647 BRXT
* Block Size: 1MB


Brexit is a digital currency that enables instant payments to anyone, anywhere in the world. Brexit uses peer-to-peer technology over ClearNet to operate with no central authority (centralisation): managing transactions and issuing currency (BRXT) are carried out collectively by the Brexit network. Brexit is the name of open source software which enables the use of the currency BRXT.



**MainNet Parameters**
P2P Port = 7511
RPC Port = 7512


Build Instructions for Qt5 Linux Wallet (Ubuntu)
================================================
//Install dependencies via Terminal:

$ sudo apt-get install make libqt5webkit5-dev libqt5gui5 libqt5core5a libqt5dbus5 qttools5-dev qttools5-dev-tools qtcreator libprotobuf-dev protobuf-compiler build-essential libboost-dev libboost-all-dev libboost-system-dev libboost-filesystem-dev libboost-program-options-dev libboost-thread-dev libssl-dev libdb++-dev libstdc++6 libminiupnpc-dev libevent-dev libcurl4-openssl-dev git libpng-dev qrencode libqrencode-dev

// Download from GIT or USE : GIT clone 
 
$ git clone git://github.com/brexitcoin/brexitcoin.git


//In terminal navigate to the Brexit-1.1.0.0 folder:

$ cd /home/Brexitcoin
or cd/home/<user>/Brexitcoin

//Then:

$ chmod -R 775 ./src/leveldb

$ qmake -qt=qt5 "USE_QRCODE=1" "USE_UPNP=1"

//Then:

$ make

//This will compile and build the Qt Wallet which takes a little while, please be patient.

//When finished you will have a file called Brexit - Simply Double Click

//end of guide

you may copy this qt file to your /usr/bin directory 

cp brexit-qt /usr/bin/

Suggestion create a shortcut on desktop to /usr/bin/britex-qt


===========================================================
Build Instructions for Terminal Based Linux Wallet (Ubuntu)
===========================================================
//Install dependencies via Terminal:

$ sudo apt-get install build-essential libboost-all-dev libssl-dev libcurl4-openssl-dev libminiupnpc-dev libdb++-dev libstdc++6 make 

//In terminal navigate to the Brexitcoin-master folder:

$ cd /home/Brexitcoin/src/

 Note : If you have trouble with leveldb , try chmod -R 775 ./leveldb/

//Enter into the terminal:

$ make -f makefile.unix USE_UPNP=1

//This will produce a file named Brexitcoind which is the command line instance of BrexitCoin

//Now type:

$ strip brexitd

//When finished you will have a file called brexitd

//To run Brexit

$ ./brexitd & 

//It will complain about having no brexit.conf file, we'll edit the one provided and move it into place

$ cd ..
$ nano brexit.conf

//Edit the Username and Password fields to anything you choose (but remember them) then save the file

$ mv brexit.conf /home/.Brexitcoin/
$ cd src/
$ ./brexitd &

//The server will start. Here are a few commands, google for more.

$ ./brexitd getinfo
$ ./brexitd getmininginfo
$ ./brexitd getnewaddresss

//end of guide
