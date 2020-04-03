# REST API Examples with curl

## **Setup**

The following examples make use of the following environment variables.

* `NODE`: Hostaddress (IP or domain name) of a chainweb node.
* `CHAINWEB_VERSION`: chainweb version to use (e.g. `development` or `testnet02`
* `CHAIN_ID`: chain id to use (e.g. 0,1,2...)
* `BLOCKHEADER_HASH`: block hash of the header the is queried
* `PAYLOAD_HASH`: hash of the payload that is queried
* `UPPER_BOUNDS`: a JSON array of block hashes. Used as upper limit (starting points) of branch queries
* `LOWER_BOUNDS`: a JSON array of block hashes. Used as lower limit (cut-off points) of branch queries
* `HEADER_ENCODING`: the accept header for selecting the block header encoding (see below)
* `NEXT`: the value of the `next` property of a result page. Used as cursor for paging endpoints.
* `LIMIT`: the maximum number of items in a requested page.

*Example setup for testnet:*

```sh
export NODE=us1.tn1.chainweb.com
export CHAINWEB_VERSION=development
export CHAIN_ID=0
export HEADER_ENCODING='-H accept:application/json;blockheader-encoding=object'
```

*Example setup for devnet:*

```sh
export NODE=us1.testnet.chainweb.com
export CHAINWEB_VERSION=testnet02
export CHAIN_ID=0
export HEADER_ENCODING='-H accept:application/json;blockheader-encoding=object'
```

## **Common Parameters**

### Block Header Encoding

*Base64 encoded JSON string:*

```sh
export HEADER_ENCODING=''
```

*JSON Object:*

```sh
export HEADER_ENCODING='-H accept:application/json;blockheader-encoding=object'
```

*Binary:*

```sh
export HEADER_ENCODING='-H accept:application/octet-stream'
```

### PAGING

Some endpoints return results in JSON object encoded pages. A page object contains the following properties:

* `items`: an array of JSON encoded result items,
* `next`: the cursor the defines the start of the next page, and
* `limit`: the number of items in the result.

Paging endpoints support the following optional query parameters:

* `next`: the start of the next page. This is a block hash prefixed with either `exclusive:` or `inclusive:`.
* `limit`: the maximum number of items in the result. The actual number of returned items may be less.

### Block Height Ranges

Endpoints that return lists of block headers or block hashes support the specification of maximum and minimum block heights for the results.

* `maxheight`: maximum block height for items included in the result
* `minheight`: minimum block height for items included in the result

## **Cut**

### GET current cut

```sh
curl -sk "https://${NODE}/chainweb/0.0/${CHAINWEB_VERSION}/cut" | python -m json.tool
```

### PUT current cut

```sh
curl -sk "https://${NODE}/chainweb/0.0/${CHAINWEB_VERSION}/cut" -XPUT -d ${CUT} | python -m json.tool
```

## **Block Headers**

### GET block header:

*Binary:*

```sh
curl -sk "https://${NODE}/chainweb/0.0/${CHAINWEB_VERSION}/chain/${CHAIN_ID}/header/${BLOCKHEADER_HASH}" -H accept:application/octet-stream | xxd -p
```

*JSON:*

```sh
curl -sk "https://${NODE}/chainweb/0.0/${CHAINWEB_VERSION}/chain/${CHAIN_ID}/header/${BLOCKHEADER_HASH}" ${HEADE_ENCODING} | python -m json.tool
```

### Query all headers in ascending order

The following queries return all block headers in the block header database including block headers on forks of the chain.

Only JSON block header encodings are supported. Binary encoding of block headers isn't supported.

*First page:*

```sh
curl -sk "https://$NODE/chainweb/0.0/${CHAINWEB_VERSION}/chain/${CHAIN_ID}/header" ${HEADER_ENCODING} | python -m json.tool
```

```sh
curl -sk "https://$NODE/chainweb/0.0/${CHAINWEB_VERSION}/chain/${CHAIN_ID}/hash" | python -m json.tool
```

*Next page:*

```sh
curl -sk "https://$NODE/chainweb/0.0/${CHAINWEB_VERSION}/chain/${CHAIN_ID}/header?next=${NEXT}" ${HEADER_ENCODING} | python -m json.tool
```

```sh
curl -sk "https://$NODE/chainweb/0.0/${CHAINWEB_VERSION}/chain/${CHAIN_ID}/hash?next=${NEXT}" | python -m json.tool
```

where `NEXT` is the value of the `next` property of the previous page.

*Page starting at `NEXT` block header of size at most `LIMIT`:*

```sh
curl -sk "https://$NODE/chainweb/0.0/${CHAINWEB_VERSION}/chain/${CHAIN_ID}/header?next=${NEXT}&limit=${LIMIT}" ${HEADER_ENCODING} | python -m json.tool
```

```sh
curl -sk "https://$NODE/chainweb/0.0/${CHAINWEB_VERSION}/chain/${CHAIN_ID}/hash?next=${NEXT}&limit=${LIMIT}" | python -m json.tool
```

### GET Genesis Block

```sh
curl -sk "https://$NODE/chainweb/0.0/${CHAINWEB_VERSION}/chain/${CHAIN_ID}/header?limit=1" ${HEADER_ENCODING} | python -m json.tool
```

```sh
curl -sk "https://$NODE/chainweb/0.0/${CHAINWEB_VERSION}/chain/${CHAIN_ID}/hash?limit=1" | python -m json.tool
```

### Query headers/hashes in descending order

These queries return all predecessors of hashes in `UPPER_BOUNDS` that are no predecessors of hashes in `LOWER_BOUNDS`. Results are returned in descending order.

Only JSON block header encodings are supported. Binary encoding of block headers isn't supported.

The endpoints accepts paging query parameters.

*POST body:*

```sh
export BOUNDS="{\"upper\":${UPPER_BOUNDS}, \"lower\":${LOWER_BOUNDS}}"
```

*Block headers:*

```sh
curl -sk "https://$NODE/chainweb/0.0/${CHAINWEB_VERSION}/chain/${CHAIN_ID}/header/branch" ${HEADER_ENCODING} -XPOST -d "${BOUNDS}" -H "content-type:application/json" -v  | python -m json.tool
```

*Block hashes:*

```sh
curl -sk "https://$NODE/chainweb/0.0/${CHAINWEB_VERSION}/chain/${CHAIN_ID}/hash/branch" -XPOST -d "${BOUNDS}" -H "content-type:application/json" -v  | python -m json.tool
```

## **Payloads**

### Without outputs

```sh
curl -sk "https://${NODE}/chainweb/0.0/${CHAINWEB_VERSION}/chain/${CHAIN_ID}/payload/${PAYLOAD_HASH}" | python -m json.tool
```

### With outputs

```sh
curl -sk "https://${NODE}/chainweb/0.0/${CHAINWEB_VERSION}/chain/${CHAIN_ID}/payload/${PAYLOAD_HASH}/outputs" | python -m json.tool
```

## **Peer Database**

### GET cut endpoint

```sh
curl -sk "https://$NODE/chainweb/0.0/${CHAINWEB_VERSION}/cut/peer" | python -m json.tool
```

### PUT cut endpoint

```sh
curl -sk "https://${NODE}/chainweb/0.0/${CHAINWEB_VERSION}/cut/peer" -XPUT -H 'content-type: application/json' -d "$PEER_INFO"
```

### GET mempool endpoints

```sh
curl -sk "https://$NODE/chainweb/0.0/${CHAINWEB_VERSION}/chain/${CHAIN_ID}/mempool/peer" | python -m json.tool
```

### PUT mempool endpoints

```sh
curl -sk "https://${NODE}/chainweb/0.0/${CHAINWEB_VERSION}/chain/${CHAIN_ID}/mempool/peer" -XPUT -H 'content-type: application/json' -d "$PEER_INFO"
```

### Compute PeerInfo

Generally, it is easier to query the peer info of a peer using a GET query for a peer database.
Otherwise the peer info can be computed as follows.

*For peers with public certificate:*

```sh
PEER_INFO="{\"address\": {\"hostname\": \"$PEER_DOMAIN\", \"port\": 443}}"
```

*For peers with self-signed Certificates:*

The peer id is the fingerprint of the certificate.

```sh
echo |
openssl s_client -showcerts -servername ${NODE} -connect ${NODE}:443 2>/dev/null |
openssl x509 -fingerprint -noout -sha256 |
sed 's/://g' |
tail -c 65 |
xxd -r -p |
base64 |
tr -d '=' |
tr '/+' '_-'
```

The peer info is created as follows:

```sh
PEER_INFO="{\"address\": {\"hostname\": \"$PEER_IP\", \"port\": 443}, \"id\": \"$PEER_ID\"}"
```
