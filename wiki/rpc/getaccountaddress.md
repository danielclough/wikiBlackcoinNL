getaccountaddress "account"

DEPRECATED. Returns the current Blackcoin address for receiving payments to this account.

Arguments:
1. "account"       (string, required) The account name for the address. It can also be set to the empty string "" to represent the default account. The account does not need to exist, it will be created and a new address created  if there is no account by the given name.

Result:
"blackcoinaddress"   (string) The account blackcoin address

Examples:
> blackmore-cli getaccountaddress 
> blackmore-cli getaccountaddress ""
> blackmore-cli getaccountaddress "myaccount"
> curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaccountaddress", "params": ["myaccount"] }' -H 'content-type: text/plain;' http://127.0.0.1:15715/

