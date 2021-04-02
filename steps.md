./geth --datadir node1 account new
Public address of the key:   0x1cBE4669A1Ba56CE94F8D4cd6831e96e04829640
Path of the secret key file: node1/keystore/UTC--2021-04-02T22-12-31.363014000Z--1cbe4669a1ba56ce94f8d4cd6831e96e04829640
----------------------------------
./geth --datadir node1 account new
Public address of the key:   0x44E56e530D788443055248faE6A74F658753f549
Path of the secret key file: node2/keystore/UTC--2021-04-02T22-13-54.854574000Z--44e56e530d788443055248fae6a74f658753f549
----------------------------------
./puppeth
----------------------------------
./geth --datadir node1 init puppeth1.json
./geth --datadir node2 init puppeth1.json
----------------------------------
./geth --datadir node1 --unlock 0x1cBE4669A1Ba56CE94F8D4cd6831e96e04829640 --mine --rpc --allow-insecure-unlock

./geth --datadir node2 --unlock 0x44E56e530D788443055248faE6A74F658753f549 --mine --port 30304 --bootnodes "enode://a4834c3f844edb51c9ea923b133b0da058dee21a4c694d8d3aefd7275e6055578b9e1eaaad328c67034b323180fdeb958b4a3b1f612833176d799ee53f89ae5b@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock

