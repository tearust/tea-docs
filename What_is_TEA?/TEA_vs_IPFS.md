# TEA vs IPFS
## TEA Uses IPFS as a File System
TEA modules do not allow saving anything to its local storage outside of temporary memory cache. All data is required to be stored in the IPFS node that it's connected to.
For the TEA Project, IPFS acts as its file system. Being  publicly accessable means that anyone can access the data as long as they know the CID. In order to protect data, everything stored to IPFS needs to be encrypted first. The encryption key will never be stored to IPFS or any persistent media. It stays in the memory of the TEA modules. You may want to ask how others access to the data since it is encrypted and keys in the TEA module. Please read more at the [following link](./TEA_vs_Trusted_Computing.md) to find out.

## TEA extends IPFS by pluging-in trusted computing module so it can run code rather than store it.
![](https://github.com/tearust/tea-docs/blob/main/res/tea-on-top-of-ipfs.png?raw=true)
Currently IPFS can only store data or code. Code is just a special format of data when it's not being executed. If your dApp needs to run the code stored in IPFS, you may have to either load it into a blockchain smart contract or a traditional cloud server to execute (AWS's Lambda FaaS will also work). The former (smart contract) execution approach is limited by existing blockchain technology. The latter (traditional cloud computing) approach relies on the centralized world. For an example, if all the cloud service providers shut down all your servers, your dApp won't run although your code/code is still remains in IPFS undamaged. I personally consider those type of "dApps" just hybrid dApps because they still rely on centralized servers to run. Decentralization is a core principle of the TEA Project and avoids centralizing too much power in the hands of the few.

TEA's solution is simple: add a trusted computing module to an existing IPFS node to turn it into a Function-as-a-service node. 

Rather than just ask IPFS to download a piece of code defined by CID, the clients can now ask IPFS (with TEA module) to *run* the piece of code (with or without input parameters) and return the result. Downloading code is using IPFS as a file system, while executing code turns IPFS into a Function-as-a-Service provider.

You may have a few questions:
- How do I verify if the result is correct?
- If the code is encrypted, how will the TEA module run the code? How about encrypted input data parameters?
- How do I know if the TEA module sends the secrets through some backdoor?

### Verifying if the Result is Correct
When an IPFS client requests a CID from the IPFS network, it doesn't need to trust whoever responds. The client can easily verify the content by verifying the hash. If the hash matches, this is exactly the data that was requested requested through the associated CID.

On the other hand, the result of code execution is unknown. You cannot verify the hash of the result to determine its correctness. In TEA, we do not verify the hash of the result, only the hash of PoT (Proof of Trust). This is done in the layer-1 blockchain. Only validated TEA nodes are allowed to host your code or data (called *pinning* in TEA nomenclature). Among those hosts, only [VRF](https://en.wikipedia.org/wiki/Verifiable_random_function) selected executor will actually run your code. The whole workflow is monitored by blockchain smart contracts. For more about the technical details of this workflow, you can read more about it here: [TEA_vs_Blockchain](./TEA_vs_Blockchain.md).

### How Can a TEA Module Run Code Stored Encrypted in IPFS?
TEA does not run the [FHE](https://en.wikipedia.org/wiki/Homomorphic_encryption) algorithm against encrypted code. FHE is too computationally expensive to be used at scale. TEA modules' CPU run plain format of code because as long as the encrypted code enter the hardware protected TEA module, it will meet the encryption key there. The computer code is decrypted and then the data is run inside this protected environment. You might wonder why is the encryption key located here? Isn't the encryption key supposed to be where the code was encrypted before posting it to IPFS? That's correct, but here is a missing piece: The [delegation chains consensus](../Under_the_hood/Delegation_chain.md) distributes the key to other safe location during the "deployment workflow". Stated another way, qualified TEA modules can "pin" or "host" your code / data before it's actually allowed to run your code. The "qualification" process is called *delegation* and it happens in the layer-1 blockchain. 

### How Do I Know That the TEA Module Doesn't Have a Backdoor to Steal My Privacy?

[Trusted computing](https://en.wikipedia.org/wiki/Trusted_Computing) has been widely used for many decades. You might not be aware that all computers and most cell phones produced in the past 10 years have a small [TPM](https://en.wikipedia.org/wiki/Trusted_Platform_Module) chip on board. This tiny chip generate PoT (Proof of Trust) data that gets validated by other nodes through consensus via smart contracts on the blockchain. 

If the computation can be loaded into the CPU's protected enclave, (a [TEE](https://en.wikipedia.org/wiki/Trusted_execution_environment) like the popular [Intel SGX](https://en.wikipedia.org/wiki/Software_Guard_Extensions), the enclave forms a protective layer for the sensitive code running inside of it. This makes the remote attestation much easier except for a compromised machine where a centralized manufacturer validation is required (Intel SGX, for example).

Using a combination of these technologies is how the 
TEA Project protects your privacy against breaches. For example, LibP2P is a part of the IPFS project which TEA uses for its network layer. This allows both IPFS and the TEA Project to share network resources. For more details on trusted computing, please read [the following article](./TEA_vs_Trusted_Computing.md).


