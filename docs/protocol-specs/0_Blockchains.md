# Blockchains as a Technological Tool

Blockchains literally mean a chain of blocks. Each block, when instantiated, stores a link to its parent block, referencing it as its parent forming an chain of data. This linking of data allows one to maintain a history of data. When multiple participants in a network maintain the corresponding data ensuring its immutability and availability, the network is said to be decentralised. Hence, blockchains are a tool that help maintain shared records.

While maintaining a chain of blocks is possible with just a key pair and a hash function, the real power of blockchains comes from the consensus mechanism that is used to agree on the next block in the chain. This consensus mechanism is what allows the network to maintain a single chain of blocks even when multiple participants are adding blocks to the chain. In todays blockchains, all blocks that follow a certain format are added to the block. However, what we want is slightly different. We want to be able to verify whether the block data follows the networks Chiti or the identities Chiti and then add the block to the chain. This requires a number of steps from block creation -> to selection of validators who can approve a block -> to the finality of the block where everyone stores a copy in their ledger.

It is beneficial for the network if the validator working on adding the block to the network himself has some skin in the game. This is measured by calculating the net stake the Validator has in the network, in terms of the aims/goals of the network.

