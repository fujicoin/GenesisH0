# GenesisH0 for Fujicoin
A python script for creating the parameters required for a unique genesis block. scrypt-N11/SHA256/X11/X13/X15.

### For Python3 and Python2

### Dependencies
    sudo pip install scrypt construct==2.5.2

### Examples
Create the original genesis hash found in Fujicoin

    python genesis.py -t 1609459200 -b 0x1e0ffff0 -n 3843000
Output:

    algorithm: scrypt
    merkle hash: f951a273c3055d1bb36b4291e7f9edd491c2d435bd5737318ef8a643cab84b61
    pszTimestamp: Mount Fuji is the most beautiful mountain in Japan, altitude is 3776.24m
    pubkey:
    time: 1609459200
    bits: 0x1e0ffff0
    Searching for genesis hash..
    1821.0 hash/s, estimate: 655.2 hgenesis hash found!
    nonce: 3843174
    genesis hash: 46e7e81bb7ab789c25594da86698fa65fbc5387d52d961a1235bcaf9d8e60f59

### Options
    Usage: genesis.py [options]
    
    Options:
      -h, --help show this help message and exit
      -t TIME, --time=TIME  the (unix) time when the genesisblock is created
      -z TIMESTAMP, --timestamp=TIMESTAMP
         the pszTimestamp found in the coinbase of the genesisblock
      -n NONCE, --nonce=NONCE
         the first value of the nonce that will be incremented
         when searching the genesis hash
      -a ALGORITHM, --algorithm=ALGORITHM
         the PoW algorithm: [scrypt|SHA256|X11|X13|X15]
      -p PUBKEY, --pubkey=PUBKEY
         the pubkey found in the output script
      -v VALUE, --value=VALUE
         the value in coins for the output, full value (exp. in fujicoin 100000000 - To get other coins value: Block Value * 100000000)
      -b BITS, --bits=BITS
         the target in compact representation, associated to a difficulty of 1

