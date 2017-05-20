### About
Forknote is innovative way to create Cryptonote (https://cryptonote.org) based cryptotokens. It gives the users the ability to create cryptotokens just by creating a simple configuration file.

### Dependencies
* GCC 4.7.3 or later     (http://gcc.gnu.org/)
* CMake 2.8.6 or later   (http://www.cmake.org/)
* Boost 1.55 or later    (http://www.boost.org/)
* MSVC 2013 (Windows only)

Step by step Windows instructions:
https://github.com/forknote/cryptonote-generator/blob/master/docs/windows-requirements-install.md

Ubuntu (tested on Ubuntu 14.04) / Mac dependencies install script:
https://github.com/forknote/cryptonote-generator/blob/master/configure.sh


### Usage
1. Download or compile the binaries
2. Create configuration file. The easiest way is to use the form on http://forknote.net
3. Start the daemon:
```
./forknoted --config-file PATH_TO_YOUR_CONFIG
```

### Configuration parameters
Create a folder in directory called configs and create a bikercoin.conf file copying parameters below; .

All fields supported:
```
EMISSION_SPEED_FACTOR=19
DIFFICULTY_TARGET=120
CRYPTONOTE_DISPLAY_DECIMAL_POINT=10
MONEY_SUPPLY=250000000000000000
GENESIS_BLOCK_REWARD=62500000000000000
SYNC_FROM_ZERO=1
DEFAULT_DUST_THRESHOLD=10000
MINIMUM_FEE=10000
CRYPTONOTE_MINED_MONEY_UNLOCK_WINDOW=10
CRYPTONOTE_BLOCK_GRANTED_FULL_REWARD_ZONE=100000
CRYPTONOTE_PUBLIC_ADDRESS_BASE58_PREFIX=63
p2p-bind-port=11882
rpc-bind-port=21882
BYTECOIN_NETWORK=2e194ef0-0135-c182-ee68-4cee4113226f
CRYPTONOTE_NAME=bikercoin
GENESIS_COINBASE_TX_HEX=010a01ff00018080d9d3b3ed826f02dd013b3b23f9f5e448e59a094b6f094d9355201f5e478fcdc4aa68b68aa83e2a2101455136a561e9b31f09670bb961adb9d7be5761e0b96e15533bdd59af413a7453
MAX_BLOCK_SIZE_INITIAL=100000
UPGRADE_HEIGHT_V2=1
UPGRADE_HEIGHT_V3=2
seed-node=174.138.56.115:11882
seed-node=174.138.56.114:11882

```

---
This code is generated by Cryptonote generator - https://github.com/forknote/cryptonote-generator
Seed source - https://github.com/amjuarez/bytecoin
start daemon using ./forknoted --config-file configs/bikercoin.conf
start simplewallet once blockchain has fully sync using ./simplewallet --config-file configs/bikercoin.conf
