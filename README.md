CrudeCoins integration/staging tree
================================

http://www.crudecoins.net

Copyright (c) 2009-2014 Bitcoin Developers
Copyright (c) 2011-2014 CrudeCoins Developers

What is CrudeCoins?
----------------

CrudeCoins is a lite version of Bitcoin using scrypt as a proof-of-work algorithm.
 - 2.5 minute block targets
 - subsidy halves in 840k blocks (~4 years)
 - ~84 million total coins

The rest is the same as Bitcoin.
 - 50 coins per block
 - 2016 blocks to retarget difficulty

For more information, as well as an immediately useable, binary version of
the CrudeCoins client sofware, see http://www.crudecoins.net.

License
-------

CrudeCoins is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the CrudeCoins
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion with the devs and community.

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/CrudeCoins/Source-Code) (https://github.com/crudecoins-project/crudecoins/tags) are created
regularly to indicate new official, stable release versions of CrudeCoins.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
    make -f Makefile.test
    ./crudecoins-qt_test
    
    CRUDE COINS EXPLORER
http://162.253.124.192:3001/

CrudeCoins addnode
162.253.124.192
162.208.10.9
162.208.8.133
192.243.103.127

How to Mine CrudeCoins

Open your wallet, and make sure you are connected to another wallet. 
 You are connected if you see the icon Wallet Connections in the lower right corner of your wallet.

The message "No block source available" will disappear once you mine your first block.

Important: replace "examplecoin" with the name of your blockchain.

Close your wallet and create the file examplecoin.conf in the folder "%APPDATA%\examplecoin\".

Paste the following text into examplecoin.conf and save the file.
rpcuser=rpc_crudecoins
rpcpassword=69c863e3356d3dae95df454a1
rpcallowip=127.0.0.1
rpcport=4210
listen=1
server=1
addnode=162.253.124.192

Download the latest version of cpuminer and extract the zip file.

Create a .bat file named mine.bat and paste the following text into mine.bat.
minerd --url=http://127.0.0.1:4210 --userpass=rpc_crudecoins:69c863e3356d3dae95df454a1

Save the file inside the extracted cpuminer folder.

Open your wallet and execute mine.bat to start mining your first coins.
    

