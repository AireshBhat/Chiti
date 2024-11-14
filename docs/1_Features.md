# Features

Chiti Features:

The main goal of the project is to allow the users to maintain a Digital Journal, a.k.a decentralised identity. While doing so, one will realise that maintaining an individual identity also implies maintaining the identities of their relationships. As mentioned in the docs before, an identity I is inseparable from its plural counterpart We.

### 1. **Secure Personal Data Storage (Digital Journal)**

Feature: Each user has a personal Digital Journal that securely stores all their identifying information and personal data.

How it Works: The Digital Journal is accessible only to the individual user, ensuring complete privacy and control over personal data.
Benefit: Users can safely store sensitive information without fear of unauthorized access or centralized data breaches.
Tech Implementation: [Willow Protocol Specifications](https://willowprotocol.org/specs/index.html#specifications)
* A Data Model for giving structured names to bytestrings. Meaning of the bytestring is decided by the identity and stored as a path. This path now acts as an attribute of the identity. A snapshot of all the paths make up the identity. A summation of the attributes produces a unique identity. Those who end up owning any data end up adding that attribute to their identity. A timer can be set to remove the corresponding data if it is temporary in nature. Providing read access to a path is akin to allowing access to a memory.
* A Capability System: To allow access to these arbitrary byte strings, a corresponding [Medowcap capability system](https://willowprotocol.org/specs/meadowcap/index.html#meadowcap), with some slight modifications to allow for blockchain integration is implemented.
* Synchronisation: A network protocol for efficiently and privately synchronising Willow data. Those systems that utilise this Chiti (identity) protocol can also perform sync operations to download data from one device to another in a secure manner utilising existing tech infrastructure such as 5G and high speed TCP/IP networks.
* [Sideloading Protocol drops](https://willowprotocol.org/specs/sideloading/index.html#sideloading) are used to create snapshot of arbitrary entries and payloads.

### 2. **Social Verification Mechanisms (Knowledge Graph)**
Feature: Users can verify their personal data and claims through a Knowledge Graph of social connections who also hold copies of relevant data.

A blockchain network is maintained to keep track of record hashes of network verifications. Each verification is like a transaction that contains what the user is attesting to and the signed message using their private key. Each transaction is identified by its unique hash which is used to create a unique CID(Hash + Metadata). Record verification hashes are sent to the network and block miners attest to transactions they witness. A separate treasury is maintained to reward miners for attesting to blocks similar to [Duniter Proof Of Work](https://duniter.org/wiki/contribute/archive/duniter-proof-of-work/) (Note: Duniter v2 uses a substrate stack to build their consensus mechanism that utilises [Web3Foundation research](https://research.web3.foundation) for consensus algorithms. Proper documentation for this hasn't been built but the code for this can be found [here](https://github.com/duniter/duniter-v2s)). Treasuries can be created by any group of people that agree on the terms and conditions of the treasury. A smart contract can be signed by multiple parties and the corresponding hash stored on the blockchain as a proof of agreement. Multiple treasury streams can be setup by the community to fund various social good activities.

How it Works: For each piece of data in a user's Digital Journal, the application records which other participants also know or can attest to that data.
Benefit: Enhances the credibility of user claims through social proof without relying on centralized authorities.

### 3. **Trust Management via Social Credit (Credit Graph)**
Feature: Users assign and manage a Credit Score in the form of a feedback rating mechanism, representing the degree of trust in them, forming a Credit Graph.

How it Works: Users allocate credit to others based on personal relationships and interactions, which can be used as social collateral for various transactions.
Benefit: Facilitates a decentralized trust network that can be leveraged for authentication, verification, and other trust-dependent activities.

### 4. **Attribute Verification Through Social Proof**
Feature: Users can verify attributes (e.g., location, qualifications) by obtaining attestations from their social network.

How it Works: A user requests verification from contacts who can confirm specific attributes. The application aggregates these attestations to strengthen the claim. Signature aggregation schemes like the Schnorr Signatures (used in current Bitcoin version) can be used to aggregate multiple signatures into a single signature. This single signature can be used to verify the authenticity of the claim.

Benefit: Provides a robust method for attribute verification that is decentralized, privacy-preserving and light weight.

### 5. **System Integrity via Liens on Credit**

How it Works: When a user makes a claim, a temporary hold is placed on the credit between participants involved in the verification or fulfillment similar to escrow contracts.
Benefit: Deters false claims and malicious behavior by introducing a cost to dishonesty, thereby enhancing trust in the system.

### 6. **Unique Identity Verification (Sybil-Resistance)**
Feature: Ensures that each participant is a unique human to prevent duplicate or fake accounts (Sybil attacks).

How it Works: Users prove their uniqueness by verifying random personal data points (e.g., past locations) through their social network, making it statistically improbable for duplicates to exist.
Benefit: Essential for applications requiring one-person-one-vote systems, fair resource allocation, and preventing spam or fraud.