# BTC-RPC Protocol
A protocol for a more secure and private light client to server pairing over Tor utilizing the Bitcoin Core JSON-RPC API. The protocol aims to be a cross platform and device agnostic reference detailing good practices to ensure interoperability between an ecosystem of light client implementations and Bitcoin Core nodes.

## Stand Up
The Stand Up implementation is the back end for the light client.

### Linux based VPS
It could be distributed as a snapshot that is easy for anyone to install with a single click. The end goal being that a user can download the light client on their mobile device then using a deep link allow a one tap Stand Up installation from a mobile web based UI, once the Stand Up script finishes the mobile device would automatically open the light client and connect to the VPS as a backend.

### MacOS Desktop App
It will be a script based program with a swift UI that installs bitcoind, tor and their dependencies on your mac. The end result being a QR code displayed to the user that they can scan with their iPhone or iPad for light client connectivity over integrated Tor.

## Light Client

### iOS
[Fully Noded](https://github.com/FontaineDenton/FullyNoded) is a proof of concept light client.
