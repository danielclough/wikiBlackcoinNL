disconnectnode "node" 

Immediately disconnects from the specified node.

Arguments:
1. "node"     (string, required) The node (see getpeerinfo for nodes)

Examples:
> blackmore-cli disconnectnode "192.168.0.6:15714"
> curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "disconnectnode", "params": ["192.168.0.6:15714"] }' -H 'content-type: text/plain;' http://127.0.0.1:15715/

