What is VuiCash?
-------------

VuiCash is a decentralized blockchain project built on Bitcoin's UTXO model, with support for Ethereum Virtual Machine based smart contracts, and secured by a proof of stake consensus model. It achieves this through the revolutionary Account Abstraction Layer which allows the EVM to communicate with VuiCash's Bitcoin-like UTXO blockchain. For more general information about VuiCash as well as links to join our community, go to https://vuicash.org

Welcome to the VuiCash Ignition Main Network. This is the main network where the tokens hold value and should be guarded very carefully. If you are testing the network, or developing unstable software on VuiCash, we highly recommend using either testnet or regtest mode. 

The major features of the VuiCash network include:

1. Compatibility with the Ethereum Virtual Machine, which allows for compatibility with most existing Solidity based smart contracts. No special solidity compiler is required to deploy your smart contract to VuiCash. 
2. A Proof of Stake consensus system which is optimized for VuiCash's contract model. Any user can stake and help to secure the network. There is no voting, master nodes, or minimum amount required. There have been transactions as small as 2 VuiCash that have created blocks in the past. 
3. The Decentralized Governance Protocol is completely implemented and functional, which allows certain network parameters to be modified without a fork or other network disruption. This currently controls parameters like block size, gas prices, etc. 
4. Uses the UTXO transaction model and is compatible with Bitcoin, allowing for existing tooling and workflows to be used with VuiCash. This allows for the infamous SPV protocol to be used which is ideal for light wallets on mobile phones and IoT devices.

Note: VuiCash Core is considered beta software. We make no warranties or guarantees of its security or stability.

VuiCash Documentation and Usage Resources
---------------

These are some resources that might be helpful in understanding VuiCash. Note that the unofficial documents are not created by the VuiCash team.

Basic usage resources:

* [Official VuiCash Usage Guide](https://github.com/yody-project/vuicash/wiki/VuiCash-Wallet-Tutorial)
* [Unofficial VuiCash staking tutorial](https://steemit.com/vuicash/@cryptominder/vuicash-staking-tutorial-using-vuicash-qt)
* [Unofficial VuiCash staking tutorial on Raspberry Pi](https://steemit.com/vuicash/@cryptominder/vuicash-staking-tutorial-using-vuicashd-on-a-raspberry-pi-3)
* [Unofficial guide for keeping your wallet safe](https://steemit.com/vuicash/@cryptominder/encrypting-backing-up-and-restoring-your-vuicash-wallet)
* [Block explorer](https://explorer.vuicash.org)
* [Unofficial block explorer](https://vuicashexplorer.io/)
* [Unofficial Raspberry Pi Web UI](https://github.com/rpiwalletui/vuicash-ui)

Development resources:

* [Deploying a custom token to VuiCash](https://blog.vuicash.org/vuicash-custom-token-walkthrough-467d725fa27d)
* [Early example faucet contract](http://earlz.net/view/2017/06/30/2144/the-vuicash-sparknet-faucet)
* [Unofficial VuiCash Hello World tutorial](https://steemit.com/vuicash/@cryptominder/quantum-vuicash-blockchain-developer-tutorial-hello-world)
* [VuiCash Book - A Developer's Guide To VUI](https://github.com/yody-project/vuicashbook)

General Info about VuiCash:

* [Mainnet event AMA](https://www.reddit.com/r/VuiCash/comments/6zs8t0/official_vuicash_ama_thread_starts_at_10pm_beijing/)
* [VuiCash's PoS vs CASPER](https://www.reddit.com/r/VuiCash/comments/788oa5/vuicashs_pos_vs_casper_and_the_nothingatstake_problem/)
* [Technical article explaining VuiCash's PoS model in depth](http://earlz.net/view/2017/07/27/1904/the-missing-explanation-of-proof-of-stake-version)
* [Unofficial What is VuiCash article](https://storeofvalue.github.io/posts/what-is-vuicash-without-the-bullshit/)

Developer's Tools
-----------------

* Smart contract deployment tool
  * https://github.com/yody-project/solar
* DApp JavaScript Library
  * https://github.com/yody-project/vuicashjs
* A toolkit for building vuicash light wallets
  * https://github.com/yody-project/vuicashjs-wallet
* CORS vuicashd RPC proxy for DApp
  * https://github.com/yody-project/vuicashportal
* Docker images for running vuicash services
  * https://github.com/yody-project/vuicash-docker
* HTTP API that powers the block explorer and the VUI web wallet
  * https://github.com/yody-project/insight-api


What is VuiCash Core?
------------------

VuiCash Core is our primary mainnet wallet. It implements a full node and is capable of storing, validating, and distributing all history of the VuiCash network. VuiCash Core is considered the reference implementation for the VuiCash network. 

VuiCash Core currently implements the following:

* Sending/Receiving VuiCash
* Sending/Receiving QRC20 tokens on the VuiCash network
* Staking and creating blocks for the VuiCash network
* Creating and interacting with smart contracts
* Running a full node for distributing the blockchain to other users
* "Prune" mode, which minimizes disk usage
* Regtest mode, which enables developers to very quickly build their own private VuiCash network for Dapp testing
* Compatibility with the Bitcoin Core set of RPC commands and APIs

Alternative Wallets
-------------------

VuiCash Core uses a full node model, and thus requires downloading the entire blockchain. If you do not need the entire blockchain, and do not intend on developing smart contracts, it may be more ideal to use an alternative wallet such as one of our light wallets that can be synchronized in a matter of seconds. 

### VuiCash Electrum

A light wallet that supports the Ledger hardware wallet and is based on the well known Electrum wallet software. 

Download: https://github.com/yody-project/vuicash-electrum/releases

### iOS and Android Wallets

These wallets run on mobile devices and synchronize quickly. 

Android Download: https://play.google.com/store/apps/details?id=org.vuicash.wallet

iOS Download: https://github.com/yody-project/vuicash-ios (open source, we are still working with Apple to get approval for their app store)

### Ledger Chrome Wallet

This light wallet runs in your Chrome browser as a browser extension. This wallet requires a Ledger device to use.

How to install: https://ledger.zendesk.com/hc/en-us/articles/115003776913-How-to-install-and-use-VuiCash-with-Ledger


Building VuiCash Core
----------

### Build on Ubuntu

This is a quick start script for compiling VuiCash on  Ubuntu


    sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils git cmake libboost-all-dev
    sudo apt-get install software-properties-common
    sudo add-apt-repository ppa:bitcoin/bitcoin
    sudo apt-get update
    sudo apt-get install libdb4.8-dev libdb4.8++-dev

    # If you want to build the Qt GUI:
    sudo apt-get install libqt5gui5 libqt5core5a libqt5dbus5 qttools5-dev qttools5-dev-tools libprotobuf-dev protobuf-compiler qrencode

    git clone https://github.com/yody-project/vuicash-bitcore --recursive
    cd vuicash

    # Note autogen will prompt to install some more dependencies if needed
    ./autogen.sh
    ./configure
    make -j2
    
### Build on CentOS

Here is a brief description for compiling VuiCash on CentOS, for more details please refer to [the specific document](https://github.com/yody-project/vuicash/blob/master/doc/build-unix.md)

    # Compiling boost manually
    sudo yum install python-devel bzip2-devel
    git clone https://github.com/boostorg/boost.git
    cd boost
    git checkout boost-1.66.0
    git submodule update --init --recursive
    ./bootstrap.sh --prefix=/usr --libdir=/usr/lib64
    ./b2 headers
    sudo ./b2 -j4 install
    
    # Installing Dependencies for VuiCash
    sudo yum install epel-release
    sudo yum install libtool libdb4-cxx-devel openssl-devel libevent-devel
    
    # If you want to build the Qt GUI:
    sudo yum install qt5-qttools-devel protobuf-devel qrencode-devel
    
    # Building VuiCash
    git clone --recursive https://github.com/yody-project/vuicash.git
    cd vuicash
    ./autogen.sh
    ./configure
    make -j4

### Additional instructions for Ubuntu 14.04

Ubuntu 14.04 has many packages that are out of date by default, so before building VuiCash you must update these:

    #update cmake from source
    sudo apt-get install build-essential
    wget http://www.cmake.org/files/v3.5/cmake-3.5.2.tar.gz
    tar xf cmake-3.5.2.tar.gz
    cd cmake-3.5.2
    ./bootstrap --system-curl
    make
    sudo apt-get install checkinstall

    # just push enter at any prompts for checkinstall
    sudo checkinstall

    #update gcc
    sudo add-apt-repository ppa:ubuntu-toolchain-r/test
    sudo apt-get update
    sudo apt-get install gcc-5 g++-5
    #update default compiler
    sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-5 1
    sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-5 1

    #install custom libleveldb (resolve -fPIC error)
    #note: this is a bit of a hack, be cautious doing this on a critical machine
    git clone https://github.com/google/leveldb.git
    cd leveldb/
    make OPT="-fPIC -O2 -DNDEBUG"
    sudo cp out-static/lib* out-shared/lib* /usr/local/lib/
    cd include
    sudo cp -r leveldb /usr/local/include/
    sudo mkdir /usr/local/include/leveldb/helpers
    cd ..
    sudo cp helpers/memenv/memenv.h /usr/local/include/leveldb/helpers
    sudo ldconfig

Additionally when using `./configure` you may need to use if you encounter errors with libmemenv.a

    ./configure --with-miniupnpc=no

### Build on OSX

The commands in this guide should be executed in a Terminal application.
The built-in one is located in `/Applications/Utilities/Terminal.app`.

#### Preparation

Install the OS X command line tools:

`xcode-select --install`

When the popup appears, click `Install`.

Then install [Homebrew](https://brew.sh).

#### Dependencies

    brew install cmake automake berkeley-db4 libtool boost --c++11 --without-single --without-static miniupnpc openssl pkg-config protobuf qt5 libevent imagemagick --with-librsvg qrencode

NOTE: Building with Qt4 is still supported, however, could result in a broken UI. Building with Qt5 is recommended.

#### Build VuiCash Core

1. Clone the vuicash source code and cd into `vuicash`

        git clone --recursive https://github.com/yody-project/vuicash-bitcore.git
        cd vuicash-bitcore

2.  Build vuicash-core:

    Configure and build the headless vuicash binaries as well as the GUI (if Qt is found).

    You can disable the GUI build by passing `--without-gui` to configure.

        ./autogen.sh
        ./configure
        make

3.  It is recommended to build and run the unit tests:

        make check

### Run

Then you can either run the command-line daemon using `src/vuicashd` and `src/vuicash-cli`, or you can run the Qt GUI using `src/qt/vuicash-qt`

For in-depth description of Sparknet and how to use VuiCash for interacting with contracts, please see [sparknet-guide](doc/sparknet-guide.md).

License
-------

VuiCash is GPLv3 licensed.

Development Process
-------------------

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/yody-project/vuicash/tags) are created
regularly to indicate new official, stable release versions of VuiCash.

The contribution workflow is described in [CONTRIBUTING.md](CONTRIBUTING.md).

Developer IRC can be found on Freenode at #vuicash-dev.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test on short notice. Please be patient and help out by testing
other people's pull requests, and remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write [unit tests](src/test/README.md) for new code, and to
submit new unit tests for old code. Unit tests can be compiled and run
(assuming they weren't disabled in configure) with: `make check`. Further details on running
and extending unit tests can be found in [/src/test/README.md](/src/test/README.md).

There are also [regression and integration tests](/qa) of the RPC interface, written
in Python, that are run automatically on the build server.
These tests can be run (if the [test dependencies](/qa) are installed) with: `qa/pull-tester/rpc-tests.py`

### Manual Quality Assurance (QA) Testing

Changes should be tested by somebody other than the developer who wrote the
code. This is especially important for large or high-risk changes. It is useful
to add a test plan to the pull request description if testing the changes is
not straightforward.
