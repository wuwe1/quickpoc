# quickpoc

easy poc template generation from the command line

## features

from the command line, call `quickpoc _addr_ _[foldername]_` to generate a ready-to-go sandbox for running POCs against mainnet.

- forge template
- src/ folder populated with all contracts and libraries
- test file autogenerated with contract import
- test set up with contract variable and mainnet forking

you can run `forge test` to confirm it's working. 

from there, simply go into `tests/POC.t.sol` and interact with the contract (stored as `c`).

## install

download the `quickpoc` file from this repo.

you can run it directly (`./quickpoc`) or, more conveniently, install it globally:
- put it somewhere you won't touch it (usually `~/bin`)
- if this folder isn't already in your path, open your bash run control file (for example, `~/.zshrc`) and add the following line: `export PATH="$PATH:/Users/path_to_folder_holding_file`
- call `chmod +x _filepath_` to make the file executable

you should then be able to call `quickpoc _addr_` from anywhere in your terminal.

note: you must be running a UNIX based machine with `bash`, `forge`, `cast`, and `jq` installed

## future

will add support for other networks if people want it.

submit issues for any features you'd like to see. 