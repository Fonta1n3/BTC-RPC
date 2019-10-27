# Stand Up
A server side one click script based installation that will setup Bitcoin Core over Tor and configure each for secure light client pairing.

## Timeline
The first priority is to build the MacOS desktop version then a linux based VPS version.

## How will it work?
It will programmatically install binaries for Bitcoin Core and Tor using script. It will configure Bitcoin Core to run with a Tor V3 hidden service which controls the nodes `rpcport`.

Upon completion the program would then display a uri link, for example:

`btcrpc://njdnkjsdkjvhs.onion?password=rpcpassword&user=rpcuser`

## Security

### Authentication
The `btcrpc://` uri is obviously extremely sensitive as anyone who has access to it would have full access to your node. The solution I propose is utilizing Tor's built in V3 cookie authentication. [Here](https://matt.traudt.xyz/p/FgbdRTFr.html) is a guide for setting up such authentication. [Fully Noded](https://github.com/Fonta1n3/FullyNoded) (the proof of concept light client) already incorporates this means of authentication and handles key generation for the user. The benefits are that the key generation process can be completely separated from the Stand Up server e.g. the bitcoind server only requires the public key, if an attacker does not have the private key used to derive the public key then the `btcrpc:\\` uri containing the hostname and rpc credentials are completely useless to the attacker. The light client should ideally create the keys locally, therefore as part of the "Stand Up" flow the user would be prompted for a public key that the light client produces.

### Wallet Encryption
The light client would handle wallet encryption and allow the user the option of wallet.dat encryption as an additional layer of security. (possibly use the auth priv key?)

### Server Security
The Stand Up server would be completely locked down with a full firewall and SSH disabled (setup a hidden service for port 22?), the only means of accessing bitcoind remotely would be via the tor hidden service.
