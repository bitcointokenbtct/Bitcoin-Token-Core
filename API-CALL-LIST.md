BTCT API Call List
=====================================

### Listing my BTCT Addresses

Listing the BTCT [address|addresses] in your wallet is easily done via `listreceivedbyaddress`. It normally lists only addresses which already have received transactions, however you can list all the addresses by setting the first argument to 0, and the second one to true.

### Full list

Required arguments are denoted inside &lt; and &gt; Optional arguments are inside [ and ].

<table>
<tr><th>Command</th><th>Parameters</th><th>Description</th><th>Requires Unlocked Wallet?</tr>
<tr><td colspan=4 align=center>Blockchain</td></tr>
<tr><td>getbestblockhash</td><td>&nbsp;</td><td>Returns the hash of the best (tip) block in the longest block chain.</td><td>N</td></tr>
<tr><td>getblock</td><td>&lt;hash&gt; [verbose]</td><td>Returns information about the block with the given hash.</td><td>N</td></tr>
<tr><td>getblockchaininfo</td><td>&nbsp;</td><td>Returns an object containing various state info regarding block chain processing.</td><td>N</td></tr>
<tr><td>getblockcount</td><td>&nbsp;</td><td>Returns the number of blocks in the longest block chain.</td><td>N</td></tr>
<tr><td>getblockhash</td><td>&lt;index&gt;</td><td>Returns hash of block in best-block-chain at index provided.</td><td>N</td></tr>
<tr><td>getblockheader</td><td>&lt;hash&gt; [verbose]</td><td>If verbose is false, returns a string that is serialized, hex-encoded data for block 'hash' header. If verbose is true, returns an Object with information about block &lt;hash&gt; header.</td><td>N</td></tr>
<tr><td>getchaintips</td><td>&nbsp;</td><td>Return information about all known tips in the block tree, including the main chain as well as orphaned branches.</td><td>N</td></tr>
<tr><td>getdifficulty</td><td>&nbsp;</td><td>Returns the proof-of-work difficulty as a multiple of the minimum difficulty.</td><td>N</td></tr>
<tr><td>getmempoolinfo</td><td>&nbsp;</td><td>Returns details on the active state of the TX memory pool.</td><td>N</td></tr>
<tr><td>getrawmempool</td><td>[verbose]</td><td>Returns all transaction ids in memory pool as a json array of string transaction ids.</td><td>N</td></tr>
<tr><td>gettxout</td><td>&lt;txid&gt; &lt;n&gt; [includemempool=true]</td><td>Returns details about an unspent transaction output.</td><td>N</td></tr>
<tr><td>gettxoutsetinfo</td><td>&nbsp;</td><td>Returns statistics about the unspent transaction output set.</td><td>N</td></tr>
<tr><td>verifychain</td><td>[numblocks=288]</td><td>Verifies blockchain database.</td><td>N</td></tr>
<tr><td colspan=4 align=center>Control</td></tr>
<tr><td>getinfo</td><td>&nbsp;</td><td>Returns an object containing various state info.</td><td>N</td></tr>
<tr><td>help</td><td>[command]</td><td>List all commands, or get help for a specified command.</td><td>N</td></tr>
<tr><td>stop</td><td>&nbsp;</td><td>Stop BTCT server.</td><td>N</td></tr> 
<tr><td colspan=4 align=center>Generating</td></tr>
<tr><td>getgenerate</td><td>&nbsp;</td><td>"PoW Only" Return if the server is set to generate coins or not. The default is false. It is set with the command line argument -gen (or btct.conf setting gen) It can also be set with the setgenerate call.</td><td>N</td></tr>
<tr><td>setgenerate</td><td>&lt;generate&gt; [genproclimit]</td><td>"PoW Only" Set 'generate' true or false to turn generation on or off. Generation is limited to 'genproclimit' processors, -1 is unlimited. See the getgenerate call for the current setting.</td><td>N</td></tr>
<tr><td colspan=4 align=center>Mining</td></tr>
<tr><td>getblocktemplate</td><td>[jsonrequestobject]</td><td>"PoW Only" Returns data needed to construct a block to work on.</td><td>N</td></tr>
<tr><td>getmininginfo</td><td>&nbsp;</td><td>"PoW Only" Returns a json object containing mining-related information.</td><td>N</td></tr>
<tr><td>getnetworkhashps</td><td>[blocks] [height]</td><td>"PoW Only" Returns the estimated network hashes per second based on the last n blocks.</td><td>N</td></tr>
<tr><td>prioritisetransaction</td><td>&lt;txid&gt; &lt;priority delta&gt; &lt;fee delta&gt;</td><td>Accepts the transaction into mined blocks at a higher (or lower) priority</td><td>N</td></tr>
<tr><td>reservebalance</td><td>[reserve] [amount]</td><td>Show or set the reserve amount not participating in network protection. If no parameters provided current setting is printed.</td><td>Y</td></tr>
<tr><td>submitblock</td><td>&lt;hexdata&gt; [jsonparamatersobject]</td><td>"PoW Only" Attempts to submit new block to network.</td><td>N</td></tr>
<tr><td colspan=4 align=center>Network</td></tr>
<tr><td>addnode</td><td>&lt;node&gt; &lt;add&#124;remove&#124;onetry&gt;</td><td>Attempts add or remove a node from the addnode list. Or try a connection to a node once.</td><td>N</td></tr>
<tr><td>clearbanned</td><td>&nbsp;</td><td>Clear all banned IPs.</td><td>N</td></tr>
<tr><td>disconnectnode</td><td>&lt;node&gt;</td><td>Immediately disconnects from the specified node.</td><td>N</td></tr>
<tr><td>getaddednodeinfo</td><td>&lt;dns&gt; [node]</td><td>Returns information about the given added node, or all added nodes.
(note that onetry addnodes are not listed here)
If dns is false, only a list of added nodes will be provided,
otherwise connected information will also be available.</td><td>N</td></tr>
<tr><td>getconnectioncount</td><td>&nbsp;</td><td>Returns the number of connections to other nodes.</td><td>N</td></tr>
<tr><td>getnettotals</td><td>&nbsp;</td><td>Returns information about network traffic, including bytes in, bytes out, and current time.</td><td>N</td></tr>
<tr><td>getnetworkinfo</td><td>&nbsp;</td><td>Returns an object containing various state info regarding P2P networking.</td><td>N</td></tr>
<tr><td>getpeerinfo</td><td>&nbsp;</td><td>Returns data about each connected network node as a json array of objects.</td><td>N</td></tr>
<tr><td>listbanned</td><td>&nbsp;</td><td>List all banned IPs/Subnets.</td><td>N</td></tr>
<tr><td>ping</td><td>&nbsp;</td><td>Requests that a ping be sent to all other nodes, to measure ping time.</td><td>N</td></tr>
<tr><td>setban</td><td>&lt;ip(/netmask)&gt; &lt;add&#124;remove&gt; [bantime] [absolute]</td><td>Attempts add or remove a IP/Subnet from the banned list.</td><td>N</td></tr>
<tr><td colspan=4 align=center>BTCT</td></tr>
<tr><td>createmasternodekey</td><td>&nbsp;</td><td>Create a new masternode private key.</td><td>N</td></tr>
<tr><td>getmasternodecount</td><td>&nbsp;</td><td>Get masternode count values.</td><td>N</td></tr>
<tr><td>getmasternodeoutputs</td><td>&nbsp;</td><td>Print all masternode transaction outputs.</td><td>N</td></tr>
<tr><td>getmasternodescores</td><td>[blocks=10]</td><td>Print list of winning masternode by score.</td><td>N</td></tr>
<tr><td>getmasternodestatus</td><td>&nbsp;</td><td>Print masternode status.</td><td>N</td></tr>
<tr><td>getmasternodewinners</td><td>[blocks=10] [filter]</td><td>Print the masternode winners for the last ''n'' blocks</td><td>N</td></tr>
<tr><td>listmasternodeconf</td><td>[filter]</td><td>Print masternode.conf in JSON format.</td><td>N</td></tr>
<tr><td>listmasternodes</td><td>[filter]</td><td>Get a ranked list of masternodes. Optional filter by txhash, status, or payment address.</td><td>N</td></tr>
<tr><td>masternodeconnect</td><td>&lt;address&gt;</td><td>Attempts to connect to specified masternode address.</td><td>N</td></tr>
<tr><td>masternodecurrent</td><td>&nbsp</td><td>Get current masternode winner.</td><td>N</td></tr>
<tr><td>masternodedebug</td><td>&nbsp</td><td>Print masternode status.</td><td>N</td></tr>
<tr><td>mnsync</td><td>&lt;status&#124;reset&gt;</td><td>Returns the sync status or resets sync.</td><td>N</td></tr>
<tr><td>spork</td><td>&lt;show&#124;active&gt;</td><td>Print raw value or active status of sporks.</td><td>N</td></tr>
<tr><td>startmasternode</td><td>&lt;local&#124;all&#124;many&#124;missing&#124;disabled&#124;alias&gt; &lt;lockwallet&gt; [alias]</td><td>Attempts to start one or more masternode(s).</td><td>Y</td></tr>
<tr><td colspan=4 align=center>Raw Transactions</td></tr>
<tr><td>createrawtransaction</td><td>[{"txid":txid,"vout":n},...] {address:amount,...}</td><td>Creates a [Raw Transactions|raw transaction] spending given inputs.</td><td>N</td></tr>
<tr><td>decoderawtransaction</td><td>&lt;hex string&gt;</td><td>Produces a human-readable JSON object for a [Raw Transactions|raw transaction].</td><td>N</td></tr>
<tr><td>decodescript</td><td>&lt;hex&gt;</td><td>Decode a hex-encoded script.</td><td>N</td></tr>
<tr><td>getrawtransaction</td><td>&lt;txid&gt; [verbose=0]</td><td>Returns [Raw Transactions|raw transaction] representation for given transaction id.</td><td>N</td></tr>
<tr><td>sendrawtransaction</td><td>&lt;hexstring&gt; [allowhighfees=false] [swiftx=false]</td><td>Submits raw transaction (serialized, hex-encoded) to local node and network.</td><td>N</td></tr>
<tr><td>signrawtransaction</td><td>&lt;hexstring&rt; [{"txid":txid,"vout":n,"scriptPubKey":hex},...] [&lt;privatekey1&gt;,...] [sighashtype=ALL]</td><td>Adds signatures to a [Raw Transactions|raw transaction] and returns the resulting raw transaction.</td><td>Y</td></tr>
<tr><td colspan=4 align=center>Utility</td></tr>
<tr><td>createmultisig</td><td>&lt;nrequired&gt; &lt;'["key",...]'&gt;</td><td>Creates a multi-signature address with n signature of m keys required.</td><td>N</td></tr>
<tr><td>estimatefee</td><td>&lt;nblocks&gt;</td><td>Estimates the approximate fee per kilobyte needed for a transaction to begin confirmation within nblocks blocks.</td><td>N</td></tr>
<tr><td>estimatepriority</td><td>&lt;nblocks&gt;</td><td>Estimates the approximate priority a zero-fee transaction needs to begin confirmation within nblocks blocks.</td><td>N</td></tr>
<tr><td>validateaddress</td><td>&lt;btct_address&gt;</td><td>Return information about the given btct address.</td><td>N</td></tr>
<tr><td>verifymessage</td><td>&lt;btct_address&gt; &lt;signature&gt; &lt;message&gt;</td><td>Verify a signed message.</td><td>N</td></tr>
<tr><td colspan=4 align=center>Wallet</td></tr>
<tr><td>addmultisigaddress</td><td>&lt;nrequired&gt; &lt;'["key",...]'&gt; [account]</td><td>Add a nrequired-to-sign multisignature address to the wallet.
Each key is a BTCT address or hex-encoded public key.
If 'account' is specified, assign address to that account.</td><td>Y</td></tr>
<tr><td>autocombinerewards</td><td>&lt;true&#124;false&gt; [threshold]</td><td>Wallet will automatically monitor for any coins with value below the threshold amount, and combine them if they reside with the same BTCT address.</td><td>Y</td></tr>
<tr><td>backupwallet</td><td>&lt;destination&gt;</td><td>Safely copies wallet.dat to destination, which can be a directory or a path with filename.</td><td>N</td></tr>
<tr><td>bip38decrypt</td><td>&lt;btct_address&gt; &lt;passphrase&gt;</td><td>Decrypts and then imports password protected private key.</td><td>Y</td></tr>
<tr><td>bip38encrypt</td><td>&lt;btct_address&gt; &lt;passphrase&gt;</td><td>Encrypts a private key corresponding to 'btct_address'.</td><td>Y</td></tr>
<tr><td>dumpprivkey</td><td>&lt;btct_address&gt;</td><td>Reveals the private key corresponding to 'btct_address'.</td><td>Y</td></tr>
<tr><td>dumpwallet</td><td>&lt;filename&gt;</td><td>Dumps all wallet keys in a human-readable format.</td><td>Y</td></tr>
<tr><td>encryptwallet</td><td>&lt;passphrase&gt;</td><td>Encrypts the wallet with &lt;passphrase&gt;.</td><td>N</td></tr>
<tr><td>getaccount</td><td>&lt;btct_address&gt;</td><td>Returns the account associated with the given address.</td><td>N</td></tr>
<tr><td>getaccountaddress</td><td>&lt;account&gt;</td><td>Returns the current bitcoin address for receiving payments to this account. If &lt;account&gt; does not exist, it will be created along with an associated new address that will be returned.</td><td>N</td></tr>
<tr><td>getaddressesbyaccount</td><td>&lt;account&gt;</td><td>Returns the list of addresses for the given account.</td><td>N</td></tr>
<tr><td>getbalance</td><td>[account] [minconf=1] [includeWatchonly=false]</td><td>If [account] is not specified, returns the server's total available balance.<br/>If [account] is specified, returns the balance in the account.</td><td>N</td></tr>
<tr><td>getnewaddress</td><td>[account]</td><td>Returns a new BTCT address for receiving payments.  If [account] is specified payments received with the address will be credited to [account].</td><td>Y</td></tr>
<tr><td>getrawchangeaddress</td><td>&nbsp;</td><td>Returns a new BTCT address, for receiving change.  This is for use with raw transactions, NOT normal use.</td><td>N</td></tr>
<tr><td>getreceivedbyaccount</td><td>[account] [minconf=1]</td><td>Returns the total amount received by addresses with [account] in transactions with at least [minconf] confirmations. If [account] not provided return will include all transactions to all accounts.</td><td>N</td></tr>
<tr><td>getreceivedbyaddress</td><td>&lt;btct_address&gt; [minconf=1]</td><td>Returns the amount received by &lt;btct_address&gt; in transactions with at least [minconf] confirmations. It correctly handles the case where someone has sent to the address in multiple transactions. Keep in mind that addresses are only ever used for receiving transactions. Works only for addresses in the local wallet, external addresses will always show 0.</td><td>N</td></tr>
<tr><td>getstakesplitthreshold</td><td>&nbsp</td><td>Returns the threshold for stake splitting.</td><td>N</td></tr>
<tr><td>getstakingstatus</td><td>&nbsp</td><td>Returns an object containing various staking information.</td><td>N</td></tr>
<tr><td>gettransaction</td><td>&lt;txid&gt; [includeWatchonly]</td><td>Get detailed information about in-wallet transaction &lt;txid&gt;.</td><td>N</td></tr>
<tr><td>getunconfirmedbalance</td><td>&nbsp;</td><td>Returns the server's total unconfirmed balance
.</td><td>N</td></tr>
<tr><td>getwalletinfo</td><td>&nbsp;</td><td>Returns an object containing various wallet state info.</td><td>N</td></tr>
<tr><td>importaddress</td><td>&lt;address&gt; [label] [rescan=true]</td><td>Adds an address or script (in hex) that can be watched as if it were in your wallet but cannot be used to spend.</td><td>Y</td></tr>
<tr><td>importprivkey</td><td>&lt;btct_privkey&gt; [label] [rescan=true]</td><td>Adds a private key (as returned by dumpprivkey) to your wallet.</td><td>Y</td></tr>
<tr><td>importwallet</td><td>&lt;filename&gt;</td><td>Imports keys from a wallet dump file (see dumpwallet).</td><td>Y</td></tr>
<tr><td>keypoolrefill</td><td>&lt;newsize&gt;</td><td>Fills the keypool.</td><td>Y</td></tr>
<tr><td>listaccounts</td><td>[minconf] [includeWatchonly=false]</td><td>Returns Object that has account names as keys, account balances as values.</td><td>N</td></tr>
<tr><td>listaddressgroupings</td><td>&nbsp;</td><td>Returns all addresses in the wallet and info used for coincontrol.</td><td>N</td></tr>
<tr><td>listlockunspent</td><td>&nbsp;</td><td>Returns list of temporarily unspendable outputs.</td><td>N</td></tr>
<tr><td>listreceivedbyaccount</td><td>[minconf=1] [includeempty=false] [includeWatchonly=false]</td><td>List balances by account.</td><td>N</td></tr>
<tr><td>listreceivedbyaddress</td><td>[minconf=1] [includeempty=false] [includeWatchonly=false]</td><td>List balances by receiving address.</td><td>N</td></tr>
<tr><td>listsinceblock</td><td>[blockhash] [target-confirmations] [includeWatchonly=false]</td><td>Get all transactions in blocks since block [blockhash], or all transactions if omitted.</td><td>N</td></tr>
<tr><td>listtransactions</td><td>[account] [count=10] [from=0] [includeWatchonly=false]</td><td>Returns up to [count] most recent transactions skipping the first [from] transactions for account [account]. If [account] not provided it'll return recent transactions from all accounts.</td><td>N</td></tr>
<tr><td>listunspent</td><td>[minconf=1] [maxconf=9999999] ['["addresses",...]']</td><td>Returns array of unspent transaction outputs with between minconf and maxconf (inclusive) confirmations. Optionally filter to only include txouts paid to specified addresses.</td><td>N</td></tr>
<tr><td>lockunspent</td><td>&lt;unlock&gt; &lt;'[{"txid":"txid","vout":n},...]'&gt;</td><td>Updates list of temporarily unspendable outputs.</td><td>Y</td></tr>
<tr><td>move</td><td>&lt;fromaccount&gt; &lt;toaccount&gt; &lt;amount&gt; [minconf=1] [comment]</td><td>Move from one account in your wallet to another</td><td>N</td></tr>
<tr><td>sendfrom</td><td>&lt;fromaccount&gt; &lt;to_btct_address&gt; &lt;amount&gt; [minconf=1] [comment] [comment-to]</td><td>&lt;amount&gt; is a real and is rounded to 8 decimal places. Will send the given amount to the given address, ensuring the account has a valid balance using [minconf] confirmations. Returns the transaction ID if successful (not in JSON object).</td><td>Y</td></tr>
<tr><td>sendmany</td><td>&lt;fromaccount&gt; {address:amount,...} [minconf=1] [comment]</td><td>Send multiple times. Amounts are double-precision floating point numbers</td><td>Y</td></tr>
<tr><td>sendtoaddress</td><td>&lt;btct_address&gt; &lt;amount&gt; [comment] [comment-to]</td><td>Send an amount to a given address. &lt;amount&gt; is a real and is rounded to 8 decimal places. Returns the transaction ID &lt;txid&gt; if successful.</td><td>Y</td></tr>
<tr><td>sendtoaddressix</td><td>&lt;btct_address&gt; &lt;amount&gt; [comment] [comment-to]</td><td>Send an amount to a given address using SwiftX. &lt;amount&gt; is a real and is rounded to 8 decimal places. Returns the transaction ID &lt;txid&gt; if successful.</td><td>Y</td></tr>
<tr><td>setaccount</td><td>&lt;btct_address&gt; &lt;account&gt;</td><td>Sets the account associated with the given address. Assigning address that is already assigned to the same account will create a new address associated with that account.</td><td>N</td></tr>
<tr><td>setstakesplitthreshold</td><td>&lt;value&gt;</td><td>This will set the output size of your stakes to never be below the given value.</td><td>Y</td></tr>
<tr><td>settxfee</td><td>&lt;amount&gt;</td><td>Set the transaction fee per kB.</td><td>N</td></tr>
<tr><td>signmessage</td><td>&lt;btct_address&gt; &lt;message&gt;</td><td>Sign a message with the private key of an address.</td><td>Y</td></tr>
</table>
