sendfrom "fromaccount" "toblackcoinaddress" amount ( minconf "comment" "comment-to" )

DEPRECATED (use sendtoaddress). Sent an amount from an account to a blackcoin address.

Arguments:
1. "fromaccount"       (string, required) The name of the account to send funds from. May be the default account using "".
2. "toblackcoinaddress"  (string, required) The blackcoin address to send funds to.
3. amount                (numeric or string, required) The amount in BLK (transaction fee is added on top).
4. minconf               (numeric, optional, default=1) Only use funds with at least this many confirmations.
5. "comment"           (string, optional) A comment used to store what the transaction is for. 
                                     This is not part of the transaction, just kept in your wallet.
6. "comment-to"        (string, optional) An optional comment to store the name of the person or organization 
                                     to which you're sending the transaction. This is not part of the transaction, 
                                     it is just kept in your wallet.

Result:
"transactionid"        (string) The transaction id.

Examples:

Send 0.01 BLK from the default account to the address, must have at least 1 confirmation
> blackmore-cli sendfrom "" "1M72Sfpbz1BPpXFHz9m3CdqATR44Jvaydd" 0.01

Send 0.01 from the tabby account to the given address, funds must have at least 6 confirmations
> blackmore-cli sendfrom "tabby" "1M72Sfpbz1BPpXFHz9m3CdqATR44Jvaydd" 0.01 6 "donation" "seans outpost"

As a json rpc call
> curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "sendfrom", "params": ["tabby", "1M72Sfpbz1BPpXFHz9m3CdqATR44Jvaydd", 0.01, 6, "donation", "seans outpost"] }' -H 'content-type: text/plain;' http://127.0.0.1:15715/

