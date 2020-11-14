# tea: Trusted Execution & Attestation
This is the root of TEA project

This repo includes the docker files to run the host, tee and client.

# Components

## tea-host
Untrusted zone. A regular server. 
### ipfs docker
Nothing but an IPFS server in docker container. No development needed
### NATS server docker
Standard NATS server. Used as the system messaging pluming system. No development needed.
### tea-layer1-docker
Substrate blockchain full node in docker container.
#### NATS client
Layer1 communicate with outside world using NATS
see [./nats-protocol.md](nats-protocol.md) for detail protocol.
#### VRF
Not resolved yet.
#### Runtime logic
TODO:

### web-nkn-nats docker
Code repo [https://github.com/tearust/tea-nkn-nats-adapter](https://github.com/tearust/tea-nkn-nats-adapter)
web-nkn-nats services provide:
- http: for bootstrap request from web initialziation, looking for active nodes.
- websocket: for webclient as long as this host has public IP
- NKN: for webclient if this host doesn't own a public IP.

For websocket and NKN, this service act as a protocol translator between WS/NKN and NATS.

The http server also works as discovery bootstrap nodes list when new client connect to. Not all host want to or can be bootstrap nodes. It has to have a public IP to be a bootstrap node. 

## tee
A small computing device to connect to the tea-host. This is trusted zone.

### tea-runtime
Code Repo [https://github.com/tearust/tea-layer1](https://github.com/tearust/tea-layer1)

### kernel
minimized linux kernel. it is just big enough to run tea-runtime and TPM driver, nothing else.

### tpm sim and rm
### wasm runtime providers
#### TPM provider
Code Repo: [https://github.com/tearust/tea-tpm-provider](https://github.com/tearust/tea-tpm-provider)
#### Layer1 provider
Code Repo: [https://github.com/tearust/tea-layer1-provider](https://github.com/tearust/tea-layer1-provider)
### wasm actors
#### Active TEE nodes list
When host request for list of current active known TEE nodes, this module will return.
This module also ping other known nodes to make sure they are still alive.

### guest actors

Nothing to mention here. Customer will upload their wasm actors.

## client dapp in general
Code Repo [https://github.com/tearust/tea-web-client](https://github.com/tearust/tea-web-client)
### hosted on IPFS IPNS

They are SPA web apps. They should be able to deploy and host at IPFS. 
They do not need a specific web server. Any IPFS nodes could feed static resources to this app.

They can be started by entering IPNS names in the browser. 

### Feed bootstrap tea nodes list

IPNS and IPFS will feed the static resources (HTML, CSS, JS) and (more important) list of bootstrap tea nodes (NKN pub key or public IP/port) to the browser and init the webapp

### Client get updated active tea nodes list from bootstrap nodes.

When webapp init, NKN client will be init first. 
webapp try to http connect any of the bootstrap tea nodes. Once connected, download existing active tea nodes. These nodes will be the candidates of "servers".

### Use WebSocket or NKN

Either https or NKN can be considered as tea's tranport layer. For those tea nodes who own a public IP, websocket is preferred.
For those who do not own a public IP, NKN can be used. 
So the tea nodes own a public IP could be more popular and profitable. (likely to be choosen as server from a client point of view).

### Server request

Once the client select one tea node as server, the client can communite with this server from now on. Including 
- send tx
- send func call req

### Potential cost of gas

We do not recommended client query information that can be calculated from client side. Only those information can NOT be calculated form client side allowed to query server.

### Switching to other active tea node as new server

In the future, every server interaction may cost some gas to discourage abuse this rule.

As a distributed system, any tea node may join and leave out of service at any time. So if one server is out of response, the client will need to choose another active nodes instead.


## client app: developer portal 

The wasm module can be either encrypted or plain. For those is encrypted format, the client can generate a random aes key. Developer need to store this aes key himself. This key will be sent to a trusted execution tee node later.
After uploading wasm to ipfs, the CID will be returned. Developer will need to save it somewhere on the client side so that it can be refered to this wasm module in the future.

If the wasm is plain. There won't be any interaction when others using his code. The smart contract will automatically caulculate the revenue and send income to developer's account.
If the wasm is encrypted, the developer has control on who will be allowed to use this code at runtime. This is only used in case-by-case computing. For example high sensitive healthcare calculation algorithm based on also sensitive medical data.
The developer will be asked to input the aes key at the time the executor tee node ready to run the code. The developer can inspect the RA result to this tee node, make sure it is qualified, then punch in the key. 
the key will be send to the executor tee node (while encrypted using the executor's tpm pub key so that no one else will get the key).
If the developer does not type in the key, the execution won't continue, b/c the key will be used to decrypte the wasm code.

## client app: consumer portal

Users can upload tasks
User can upload data. Data is used by the algorithm to run against. The data should be encrypted. Consumer owns the key. Only provide the key when he is satisfied on the exeuctor tee's PoT.
User can pay for use

# Installation
## NATS server docker 
ref to https://docs.nats.io/nats-server/nats_docker
```
docker pull nats
docker run nats
```
NATS will carry communication between different components **inside** the host or **between** the host and tee. So the TLS is not needed.
The host should NOT expose the NAT's port (by default 4222) to the public.
## IPFS server docker
Ref: https://hub.docker.com/r/ipfs/go-ipfs
```
docker pull ipfs/go-ipfs
docker run -d --name ipfs_host -v $ipfs_staging:/export -v $ipfs_data:/data/ipfs -p 4001:4001 -p 127.0.0.1:8080:8080 -p 127.0.0.1:5001:5001 ipfs/go-ipfs:latest

```


