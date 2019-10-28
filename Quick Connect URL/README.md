# Quick Connect URL
 This section will define the spec for the deep link URI and QR Code which ideally would have the same format to ensure universal compatibility with either deep links or QR code scanning.

## Current Format
An example URL following the current format is:

`btcrpc://<rpcuser>:<rpcpassword>@<hidden service hostname>:<hidden service port>?label=<optional node label>&v2password=<optional v2 password>``

Example with label and v2password:

`btcrpc://rpcuser:rpcpassword@kjhfefe.onion:8332?label=nodeName&v2password=uenfieufnuf4`

Example without label and v2password:

`btcrpc://rpcuser:rpcpassword@kjhfefe.onion:8332`

This allows node manufacturers the option of hard coding a label for the node. There ideally would be a two factor authentication where user inputs the V2 or V3 auth cookie into the client app manually so that if the URL leaks somehow it would not give an attacker access to the node.
