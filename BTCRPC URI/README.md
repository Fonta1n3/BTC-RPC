# BTC-RPC
 This section will define the spec for the deep link URI and QR Code which ideally would have the same format to ensure universal compatibility with either deep links or QR code scanning.

## Current Format
An example URI following the current format is:

`btcrpc://wjdnowndv7h47f4f7hf3jf9nffk.onion:8332?user=therpcuser&password=therpcpassword`

Currently this is in its nascent stages, the only light client that exists which has adopted this is [Fully Noded](https://github.com/Fonta1n3/FullyNoded) and the only server side node manufacturer supporting it is [Nodl](https://www.nodl.it) (to be released soon). Due to the simplicity of embedding such a link into a web based UI it is my hope more node manufacturers will adopt this as a standard, as it allows seamless "one tap" light client connectivity over Tor to their node (assuming the user taps the deep link from their device which has the compatible light client installed).
