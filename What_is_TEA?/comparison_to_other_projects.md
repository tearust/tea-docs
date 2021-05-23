# Competition, especially in comparison with the projects invested by competitors
## Comparison to Dfinity
Difference between TEA project and Dfinity:

Dfinity does not rely on secure hardware. It uses cryptography and consensus solutions. There are both advantages and disadvantages to this; Dfinity can be proved mathematically, but still consumes a lot of computing resources and is not suitable for edge nodes to participate. It also still needs infrastructure similar to the cloud computing center. General public miners are not likely to participate. Potential risks are re-centralized
TEA Project relies on cheap security chips, and does not require expensive CPU, GPU, ASIC, hard disk or other equipment. TEA mining machine is currently positioned as a single-board computer + TPM security chip mining machine solution of less than one hundred dollars. This is because TEA does not require high-energy-consuming complex cryptographic computing and consensus algorithms. This is convenient for the public to participate in mining, and it may even be built into set-top box routers or even refrigerator, washing machines in the future. This can avoid re-centralization. The disadvantage is that it is not easy to get agreement from scholars and researchers.

## Comparison to IPFS/FileCoin
The difference between TEA Project and IPFS (FIL)

IPFS is only responsible for storage and network, FIL needs to consume hard drives to compete for mining. 
TEA Project runs on IPFS, utilizing storage and network provided by IPFS to extend trust computing features for IPFS.  

In fact, TEA is an ideal add-on module of IPFS. It can rely on the established IPFS miners to quickly form a computing power market. For IPFS miners, adding some cheap TEA mining machines, they can do dual mining on the IPFS mining machine. 

IPFS and TEA Project are not competitors. TEA Project relies on IPFS and provides computing power for IPFS. Thus, IPFS will become a true decentralized Internet computing node rather than just storage. 

## Comparison to Other CPU Trust Hardware Project (iEXEC, Phala, etc)
Basically all blockchain projects that also apply to trusted hardware use CPU trusted technology such as Intel SGX. For example, iEXEC, Phala, etc. Compared with this type of projects, there are these differences:

This type of projects rely on Intel to provide security certification, Intel will become the new center. Decentralization is not thorough enough. TEA Project does not use CPU technology, instead, it uses extremely cheap and TPM-Trusted Computing technology. Because this technology has been popular for 20 years and manufacturing processes have been simplified, a lot of suppliers are available and decentralized.
The TEE programming for the CPU is on the bottom layer. The average application developer cannot master such a bottom layer technology. It is not conducive to the participation of ordinary application developers. The TEA Project does not require developers to understand any trusted hardware underlying. It only requires them to use common language to compile program functions into Web Assembly format and then reprint on TEA nodes for calculations. This greatly reduces the entry barrier. 
Intel’s CPU cost and power consumption are both very high. Relatively speaking, all computers produced after 2008 have TPM chips. Because of its simple design and no production threshold, the cost becomes extremely low. It can be used in miniature low-power IoT. Thus, real nationwide computing and edge computing can be realized on the device.
The TPM chip used by TEA Project does not participate in the computing. Therefore, many specialized heterogeneous computing types can be used. For example, the specialized TensorFlow processor TPU for artificial intelligence, the image processor GPU, and the new Risc-V processor can be used on TPM-protected hardware, but Intel CPUs cannot coexist.
