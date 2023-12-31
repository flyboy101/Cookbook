# Cookbook
## Bitcoin Core:
### Resources
- [Jon Atack - How to review pull requests](https://jonatack.github.io/articles/how-to-review-pull-requests-in-bitcoin-core)
- [Chaincode Labs study guide](https://github.com/chaincodelabs/seminars)



## Bitcoin Wallet:
### HD wallet key identifier (path)
HD wallet key identifier (path)
Keys in an hardware wallet are identified using a "path" convention, with each level of the tree separated by a slash (/) character. Private keys derived from the master private key start with "m." Public keys derived from the master public key start with "M." Therefore, the first child private key of the master private key is m/0. The first child public key is M/0. The second grandchild of the first child is m/0/1, and so on.
The "genealogical tree" of a key is read from right to left, until you reach the master key from which it was derived. For example, identifier m/x/y/z describes the private key that is the z-th child of the parent private key m/x/y, which is the y-th child of the parent private key m/x, which is the x-th child of the parent master private key m.


Hardware wallet path examples
|HD path | Key described|
| ------ | ------ |
| m/0 | The first (0) child private key from the master private key (m)|
| m/0/0 | The first (0) child private key from the first child (m/0)|
| m/0'/0 | The first (0) normal child from the first _hardened_ child (m/0')|
| m/1/0 | The first (0) child private key from the second child (m/1)|
| M/23/17/0/0 | The first (0) child public key from the first child (M/23/17/0) from the 18th child (M/23/17) from the 24th child (M/23)|

BIP-44 specifies the derivation path structure as consisting of five predefined tree levels:
```
m / purpose' / coin_type' / account' / change / address_index
```
- The second-level `coin_type` specifies the type of cryptocurrency coin, allowing for multicurrency HD wallets where each currency has its own subtree under the second level. For example, for Bitcoin it is m/44'/0'.
- The third level of the tree is `account` which allows users to subdivide their wallets into separate logical subaccounts, for accounting or organizational purposes. For example, an hardware wallet might contain two bitcoin accounts: m/44&#x27;/0&#x27;/0&#x27; and m/44&#x27;/0&#x27;/1&#x27;. Each account is the root of its own subtree. Changing the value for `account` you can generate as many wallets as you wish, for example:
```
m/84'/0'/0'/0
m/84'/0'/1'/0
m/84'/0'/2'/0
m/84'/0'/94982'/0
```
- On the fourth level, `change`, an hardware wallet has two subtrees, one for creating receiving addresses and one for creating change addresses. Note that whereas the previous levels used hardened derivation, this level uses normal derivation. This is to allow this level of the tree to export extended public keys for use in a nonsecured environment. Usable addresses are derived by the hardware wallet as children of the fourth level, making the fifth level of the tree the "address_index." For example, the third receiving address for bitcoin payments in the primary account would be M/44&#x27;/0&#x27;/0&#x27;/0/2. 


# Send later email in Gmail:
Free sources:
 - GMailSendLater: https://github.com/devietti/GmailSendLater

Dependences:
 - Date & Time picker: https://github.com/T00rk/bootstrap-material-datetimepicker



Trader based on google finance data and google spreadsheet

For further info on how to set up a readme file in Github:
 - https://guides.github.com/features/mastering-markdown/
 - https://guides.github.com/features/wikis/#creating-a-readme

On how to setup a web page in Github:
 - https://pages.github.com/
 
On Bitcoin and beyond:
 Mastering Bitcoin
 - https://github.com/bitcoinbook/bitcoinbook
 
