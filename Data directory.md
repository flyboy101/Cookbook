# Directory content
## Files
An overview of these is in [files.md](https://github.com/bitcoin/bitcoin/blob/master/doc/files.md) in the Bitcoin Core documentation.

## Personally identifiable data
This section may be of use to you if you wish to send a friend the blockchain, avoiding them a hefty download.

Subdirectory       | File(s)               | Safely deleted | Description
-------------------|-----------------------|----------------|-------------
`-`                | `bitcoin.conf`        | NO  | May contain your IP or hidden service address, paths on your filesystem, and RPC credentials.
`-`                | `settings.json`       | NO  | Contains GUI settings with a similar nature to those in bitcoin.conf.
`-`                | `debug.log`           | Yes | May contain IP addresses and transaction ID's. 
`-`                | `wallet.dat`          | Make backup | Contains addresses and transactions linked to them. 
`-`                | `db.log`              | Yes | May contain information pertaining to your wallet. 
`database/ folder` | `-`                   | -   | This should only exist when bitcoin-qt is currently running. It contains information (BDB state) relating to your wallet.
`-`                | `peers.dat`           | Yes | It contains addresses and connection statistics of peers, but does not contain any personally identifiable data. 
`.cookie`          |                       | Do not share with others  | Contains temporary RPC credentials in situations where you haven't specified an explicit username & password. 
`-`                | `onion_v3_private_key`| Do not share with others | Contains your hidden service key if you are running Bitcoin Core through a Tor connection. 
  



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
