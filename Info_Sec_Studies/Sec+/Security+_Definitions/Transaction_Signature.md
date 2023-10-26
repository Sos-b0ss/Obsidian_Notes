Sources:
https://documentation.solarwinds.com/en/success_center/orionplatform/content/ha_transaction_signatures.htm
https://wiki.trezor.io/Transaction_signature
\
This topic explains what transaction signatures are. SolarWinds requires transaction signatures ([[TSIG]]) when interacting with [[BIND]] [[DNS]] instead of administrator credentials. [[TSIG]] grants greater security when updating the [[DNS]] server. The [[TSIG]] shared secret key name is the name you gave the key in the configuration file.
\
A transaction signature is needed when sending a transaction to the network. Signed transaction confirms that the sender owns the private key associated with the address and, therefore, owns the funds. Anyone in the network can verify the transaction.
