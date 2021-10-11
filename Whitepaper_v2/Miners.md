      

The TEA module, a small cheap computing unit with a TPM chip built-in, connects to IPFS only. It relies on IPFS and LibP2P to provide storage and network. TEA modules connect to other TEA modules using a secured connection (security keys protected by TPM hardware) forming a layer-2 network. Although physically, all information between TEA modules needs to go through the IPFS network, and the communication is worry-free due to hardware encryption.


All computational work including decryptions are processed inside the hardware-protected secure module. The TPM monitors the entire hardware even before the system boots. All the critical security evidence is stored in TPM as PoT. The PoT will be sent to layer-1 blockchain for Remote Attestation by other VRF selected "known good" TEA nodes. The consensus is done at the blockchain layer (we call the blockchain layer layer-1). The clients only need to query the layer-1 blockchain to verify the PoT is posted in a valid block so that they can trust the correctness of the computing result.

