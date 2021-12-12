**reach out at** :bird: [@gpestana](https://twitter.com/gpestana) / :globe_with_meridians: [gpestana.com](https://www.gpestana.com/)

---

Current research projects on privacy, web security and P2P networks and applied cryptography. **Reach out if you'd like to learn more, collaborate or discuss!**.

- [IPFS-SBC: IPFS as a practical Secure Broadcast Channel](#IPFS-SBC-IPFS-as-a-practical-Secure-Broadcast-Channel)
- [p3lib: Privacy enhanced routing and content discovery on IPFS](#p3lib-Privacy-enhanced-routing-and-content-discovery-on-IPFS)
- [NR2P - Non-repudiable and publicly verifiable TLS session data](#NR2P---Non-repudiable-and-publicly-verifiable-TLS-session-data)
- [Trusted computing on untrusted platforms](#Trusted-computing-on-untrusted-platforms)
- [Verifiable and privacy-preserving humanity attestation based on blockchain activity](#Verifiable-and-privacy-preserving-humanity-attestation-based-on-blockchain-activity)
- [Cryptographic black-box accumulators as privacy-preserving humanity proofs for the web](#Cryptographic-black-box-accumulators-as-privacy-preserving-humanity-proofs-for-the-web)

### IPFS-SBC: IPFS as a practical Secure Broadcast Channel

https://www.gpestana.com/papers/sbc-ipfs-draft.pdf

We design, implement and study a decentralized secure broadcast encryption channel (SBC) on the InterPlanetary File System (IPFS) protocol stack. The SBC leverages a cryptographic broadcast encryption scheme that allows a set of participants (the sources) to encrypt messages with capabilities that only a subset of receivers can decrypt. The encrypted mes-sage is then published on a public channel where all the receivers attempt to recover the plaintext of the encrypted message. The decryption is successful only for the subset of receivers selected by the source. Furthermore, the SBC guarantees that every reader has the same view of the messages published in the broadcast channel and that the published messages are not tampered.This technical report shows that the IPFS protocol stack can be used to implement a practical and decentralized SBC. We demonstrate that the properties provided by the IPFS protocol stack such as data integrity, availability, censorship resistance,decentralization and available pub-sub semantics can be lever-aged to implement a practical and secure broadcast encryption channel that can be used by a wide array of applications.Moreover, we implement SBC-IPFS, a decentralized and secure broadcast encryption channel and study its bandwidth overhead and performance in the context of real-world applications.

### p3lib: Privacy enhanced routing and content discovery on IPFS

https://github.com/gpestana/p3lib

Currently, Brave integrates a native IPFS node that allows users to fetch and seed content on the IPFS network through the network. The IPFS node also allows users to interact with content stored in IPFS as if it was HTTP content. For example, when visiting `ipfs://<CID>` the browser will fetch the blocks of the respective CID (content ID) and treat it as a native webpage. However, during the IPFS onboarding in the browser, we highlight that Brave cannot offer the privacy guarantees that are provided by design in all other browser components. The main reason is that the IPFS protocol is inherently leaky with regards to the content that peers seed and search for and, by default, peers have a long-lived identity. Thus, by actively or passively monitoring network requests on IPFS, it is possible to learn insights about IPFS users that allow attackers to learn users’ interests and behavior over time. This line of research aims at motivating, designing and developing privacy enhancing protocols for IPFS that can be implemented in the context of the browser. In addition, we aim to concretely define and formalize a framework around how to reason about privacy of DHT-based P2P networks and respective threat models, and use IPFS as a widely deployed and used network as a benchmark.

### NR2P - Non-repudiable and publicly verifiable TLS session data

https://hackmd.io/35kzObpuQH6n4MQ_QtrQ3g

The TLS protocol relies on symmetric cryptography to encrypt data in the wire between the client and the origin. Symmetric cryptography is used for performance reasons. However, since the session data is encrypted with a secret key agreed between the origin and the client, it is not trivial to build a scheme where the client proves the authenticity of TLS data with an origin to a third-party. Some schemes (e.g. [DECO protocol](https://deco.works/)) have attempted to circumvent this limitation by changing the TLS handshake between the origin and the client by introducing the verifier as part of the handshake and relying on multiparty computation between the the three participants. The goal of the three-party TLS handshake is to allow the client and the verifier to commit to the secret key of the TLS handshake without having to change any TLS server-side code. Once the TLS session key is committed, the verifier can verify any proof of authenticity over the TLS data that the user provides. This scheme allows also the user to generate zero knowledge proofs over encrypted TLS session that is impossible to forge by the user. However, the three party computation scheme introduces massive performance penalties and complecity. In this work, we take another path towards verifiable and unforgeable TLS data. We design and implement NR2P (Non-Repudiable Record Protocol), which replaces the symmetric key encryption with an asymmetric key encryption scheme in TLS 1.3. We show how to implement the server and client-side code so that it is backwards compatible with vanilla TLS 1.3. In addition, we show how the user can generate arbitrary zero-knowledge proofs based on encrypted TLS data from an origin that can be publicly verifiable. 

### Trusted computing on untrusted platforms

We define a protocol that allows a server (verifier) to request clients (provers) to run obfuscated instructions without revealing the instruction logic. The protocol enables running trusted computation on untrusted platforms with strong security and privacy guarantees for both the verifier and the prover. The protocol has the following strong guarantees: i) the client must be able to prove the validity and correctness of the output of the obfuscated computation to the verifier, given a set of private (to the verifier) and public inputs; and ii) the client can learn the amount of information (i.e. number of bits) that the output "leaks" to the verifier. We assume the client to be curious and potentially an active attacker: i.e., the client has incentives to de-obfuscate the logic running locally and to attempt to tamper the results of the computation. We implement two instantiations of the scheme: one that leverages binary obfuscation and cryptographic signatures and another that relies on zero knowledge frameworks to achieve similar results.

### Humanity tokens: Verifiable and privacy-preserving humanity attestation based on blockchain activity

This research work focus on designing and implementing publicly verifiable proofs based on blockchain data that can be used to protect Sybil attacks and as a humanity attestation (similar to web CAPTCHAs). Humanity tokens are proofs generated based on semi-public blockchain activity that can be verifiable non-interactively publicly. User are able to generate claims such as "I know the private key that has made X transactions in the past N blocks on blockchain X" and "I know the private key that has performed action X, Y, Z on blockchain X". Since on-chain activity is expensive and not easy to replicate at current the scale necessary for current botnets, humanity tokens/proofs can be used as humanity attestation and Sybil prevention by web services.

### Cryptographic black-box accumulators as privacy-preserving humanity proofs for the web

We design and implement a cryptographic blackbox accumulator scheme that allow users to accumulate signatures from multiple third parties. The state of the accumulator can be used to generate zero knowledge proofs of reputation.
