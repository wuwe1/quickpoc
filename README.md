# quickpoc

easy POC template generation from the command line

## features

from the command line, call `quickpoc 0x.. [folder_name]` to generate a ready-to-go sandbox for running POCs for the given address against mainnet, including:

- forge template with name mirroring contract name
- `src/` folder populated with all contracts and libraries
- test file autogenerated with contract import
- test setup with contract variable and mainnet forking
- `cd folder_name` copied to clipboard to save you 1 extra second

you can run `forge test` to confirm it's working, then go into `tests/POC.t.sol` to interact with the contract (saved in storage as `c`).

## install

note: you must be running a UNIX based machine with `bash`, `forge`, `cast`, and `jq` installed.

1) download the `quickpoc` file from this repo.

2) set up two environment variables by calling the following from your terminal:
- `export ETH_RPC_URL="..."`
- `export ETHERSCAN_API_KEY="..."`

3) you can then run it directly by calling the file (`./quickpoc`) 

4) more conveniently, install it globally:
- put it somewhere you won't touch it (usually `~/bin`)
- if this folder isn't already in your path, open your bash run control file (for example, `~/.zshrc`) and add the following line: `export PATH="$PATH:/Users/path_to_folder_holding_file`
- call `chmod +x path_to_file` to make the file executable
- you should then be able to call `quickpoc 0x..` from any folder to generate the POC folder within it.

## future

- [ ] support non-mainnet networks
- [ ] allow inputting multiple addresses
- [ ] automatically pull all contracts listed on an immunefi page

please submit issues for any additional features you'd like to see :)

## thank yous

big thanks to [deliriusz](https://github.com/deliriusz) for adding graph viz tools, proxy checks, and professionalism. 