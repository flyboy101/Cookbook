# Directory content
## Files
An overview of these is in [files.md](https://github.com/bitcoin/bitcoin/blob/master/doc/files.md) in the Bitcoin Core documentation.

## Personally identifiable data
This section may be of use to you if you wish to send a friend the blockchain, avoiding them a hefty download.

Subdirectory       | File(s)               | Safely deleted | Description
-------------------|-----------------------|----------------|-------------
`-`                | `bitcoin.conf`        | NO  | May contain your IP or hidden service address, paths on your filesystem, and RPC credentials.
`-`                | `settings.json`       | NO  | Contains GUI settings with a similar nature to those in bitcoin.conf.
`-`                | `anchors.dat`         | -   | 
`-`                | `peers.dat`           | Yes | It contains addresses and connection statistics of peers, but does not contain any personally identifiable data. 
`-`                | `mempool.dat`         | -   | 
`-`                | `debug.log`           | Yes | May contain IP addresses and transaction ID's. 
`-`                | `wallet.dat`          | Make backup | Contains addresses and transactions linked to them. 
`-`                | `db.log`              | Yes | May contain information pertaining to your wallet. 
`database/ folder` | `-`                   | -   | This should only exist when bitcoin-qt is currently running. It contains information (BDB state) relating to your wallet.
`.cookie`          |                       | Do not share with others  | Contains temporary RPC credentials in situations where you haven't specified an explicit username & password. 
`-`                | `onion_v3_private_key`| Do not share with others | Contains your hidden service key if you are running Bitcoin Core through a Tor connection. 
`blocks`           | `-`                   | -  | Contain information pertaining only to the public blockchain. This directory ist cross-platform, i.e. it can be copied between different installation
`chainstate`       | `-`                   | -  | Contain information pertaining only to the public blockchain. This directory ist cross-platform, i.e. it can be copied between different installation
`blocks/index`     | `-`                   | -  | Contain information pertaining only to the public blockchain
  
# Transferability

Each node has a unique block database, and all of the files are highly connected. So if you copy just a few files from one installation's "blocks" or "chainstate" directories into another installation, this will almost certainly cause the second node to crash or get stuck at some random point in the future. If you want to copy a block database from one installation to another, you have to delete the old database and copy all of the files at once. Both nodes have to be shut down while copying.



#
#
#
#
#
#
#
#
#
#
#
#
