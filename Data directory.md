# Directory content
## Files
An overview of these is in [files.md](https://github.com/bitcoin/bitcoin/blob/master/doc/files.md) in the Bitcoin Core documentation.

## Personally identifiable data
This section may be of use to you if you wish to send a friend the blockchain, avoiding them a hefty download.

- wallet.dat

  Contains addresses and transactions linked to them. Please be sure to make backups of this file. It contains the keys necessary for spending your bitcoins. You should not transfer this file to any third party or they may be able to access your bitcoins.
  
- db.log

  May contain information pertaining to your wallet. It may be safely deleted.
  
- debug.log

  May contain IP addresses and transaction ID's. It may be safely deleted.
  
- database/ folder

  This should only exist when bitcoin-qt is currently running. It contains information (BDB state) relating to your wallet.

- peers.dat

  It contains addresses and connection statistics of peers, but does not contain any personally identifiable data. It may be safely deleted.
  
- bitcoin.conf

  May contain your IP or hidden service address, paths on your filesystem, and RPC credentials.
  
- settings.json

  Contains GUI settings with a similar nature to those in bitcoin.conf.
  
- .cookie

  Contains temporary RPC credentials in situations where you haven't specified an explicit username & password. Do not share with others.
  
- onion_v3_private_key

  Contains your hidden service key if you are running Bitcoin Core through a Tor connection. Do not share with others or they will be able to spoof your .onion address. On older versions of Core this file was called onion_v2_private_key.



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
