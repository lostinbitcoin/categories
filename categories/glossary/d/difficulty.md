---
title: 難易度
taxonomy:
    category:
        - d
---

## Difficulty
2,100 sats

The difficulty is a measure of how hard it is to mine a block. In order to mine a block, miners must provide Proof-of-Work in the form of a valid hash of the block they intend to publish. A hash is essentially a large number, and for a hash to be valid, it must be smaller than a defined target number. This target number determines the difficulty of mining and is set by Bitcoin’s ruleset. This difficulty is dynamic: it updates every 2016 blocks—roughly 2 weeks—to ensure Bitcoin blocks come in roughly every 10 minutes. If more miners join the network and mine blocks at a faster rate, difficulty will rise. If miners stop mining, and blocks arrive slower than every 10 minutes, difficulty will fall. The difficulty therefore directly follows the trend in hash rate of the network. In a technical sense, the Bitcoin network sets the target rather than the difficulty. All valid Proofs-of-Work must be below this target. The difficulty then, is simply the inverse of the target. If the target is raised, this makes it easier for miners to find a hash below the target, so the difficulty has been lowered. Likewise, if the target is lowered, the difficulty has been raised. The target is encoded as a part of each block header and is called the ‘bits’ of a block. This allows nodes to directly verify whether the Proof-of-Work provided for a block is lower than the target.

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
