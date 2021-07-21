# Availability, Reliability, Robustness - All Technically Achievable With the TEA Project
The design concept and philosophy of the TEA Project is very innovative.
**TEA is not trying to improve consensus but to allow each blockchain layer to do what it's best at.**

Unlike other projects, the TEA project doesn't try to improve the consensus of the blockchain. It instead allows the consensus algorithm to do what it's most suitable for. Consider the following analogy: 

>A security guard stands at the door of an institution. The duty of a security guard is to ensure that only authorized personnel can enter and to keep outsiders from entering the door. The security guard does not need to understand or be good at the professional business of the institution. He only needs to stand on guard. In this way, the goal of security is achieved while paying a security guard's salary (and not the higher salary of a hardware engineer).

The TEA Project is like this, for it only allows the blockchain consensus to process the PoT (Proof of trust) data provided by the hardware of the layer-2 nodes rather than processing the customers' code logic. Therefore, the existing blockchain speed is sufficient for such a simple task. The truly complex customer business logic runs in the secure layer-2 trusted computing environment.

## Less is More
Another important design principle is "less is more." From the perspective of computer security, as long as the TCB (Trusted Code Base) that needs to be protected is large and complex, the attack surface is too large for it to be considered safe. Therefore, the TEA project is very simple by design. 

TPM is a security chip that's well designed in that it's basically too simple to be attacked. It's become a secure technology used by numerous devices that have been running for many years. In order to apply this simple design principle to the other levels of the technology stack, the TEA Project has further streamlined the NixOS operating system. NixOS is a special streamlined Linux release known for its security. It's not only removed many unnecessary operating system modules, it's also removed the network modules that are often considered essential. In this way, there is no network in the TEA security domain. Without a network to access, hackers cannot initiate remote attacks against the trusted area of TEA through the network stack. At the application layer, it's only strictly required that WebAssembly code can run on the TEA-runtime. The security of the entire system has been strengthened again by using the security language of WebAssembly itself. These approaches have not raised the barrier for developing applications on the TEA ecosystem.

## Economics Beats Technologies
The last and equally important design principle is using economic design to change the principle of security protection. The aim is to disincentivize hackers instead of focusing on making everything impervious from attack. The TEA Project uses a number of mature cryptography technologies to randomize the computing process and anonymize secret substitution, thereby greatly increasing the difficulty of any attacks and the probability of any vulnerabilities being exploited. These all add to an attacker's costs, helping make the TEA network 'too expensive to attack.'

# Current Project Status (July,  2021)
The TEA Project has already completed a successful demo on a simulator. This demo implements an artificial intelligence computing task on the blockchain under the premise of protecting data and code privacy. This demo video is still on the TEAProject.org website.

Because TEA's main network has not yet been publicly operated, there is still a lack of actual operating evidence while discussing its robustness. Currently, it is only possible to speculate on its safety, reliability and robustness through design ideas, principles, and codes.

Since TEA Project did not invent new consensus algorithms or encryption technologies that require mathematics or time-proof, it uses a large number of security technologies that have proven mature over a number of years (such as TPM). Although very new, it already integrates a broad range of open-source community-based mature technologies (like IPFS and WebAssembly). There is also already a prototype demo that can be run, making there little doubt that the TEA Project is legitimate.

The TEA Project leverages redundant hardware design through a distributed system composed of a large number of TEA nodes. It can be speculated that it has high reliability and robustness and can tolerate no more than 1/3 of its nodes failing or suffering Byzantine faults.