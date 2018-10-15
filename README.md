### To signup for the airdrop:
`cleos push action deltadextoken signup '{"owner":"owneraccount","quantity":"0.0000 DEX"}' -p owneraccount@active`

The signup function allows an account to create a balance entry using their own personal ram.


### To burn tokens run the command:
`cleos push action deltadextoken burn '{"from":"owneraccount","quantity":"1.0000 DEX","memo":"Lets remove DEX supply!"}' -p owneraccount@active`

The burn function burns the token from the "from account" and also reduces the supply.

The burn function makes sure you can't burn more tokens than supply.

The burn function has been modified to allow you to burn your zero balance if you don't want to wait for the airdrop.

### Guarantee you don't pay ram

Two additional commands have been added:

1. issuefree
1. transferfree

These commands work the same as issue and transfer, however they fail if the destination does not have a table row already.

The purpose of this is to prevent you accidentally paying RAM for accounts that unregister from the airgrab (via burn) after you've taken a snapshot.
