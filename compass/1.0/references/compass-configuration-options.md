# Compass configuration options

**The Compass configuration options allow you to customize your private Tangle, depending on your needs. For example, you could create a lightweight private Tangle for a specific test, or create a more resource intensive one that's similar to the Mainnet.**

|**Parameter**|**Description**|**Notes**|
|:----------------------|:--------------|:--------|
|`seed` |Seed that Compass uses to sign milestone bundles |Back up this seed and keep it secure|
|`security`|Security level of Compass' signatures|The greater the security level, the larger and more secure the signature of a spent address is against brute force attacks. A greater security level also means that more computations must be done to sign a bundle and that more transactions are needed in a bundle to contain the signature. As a result, low-powered devices may want to use security level 2, whereas a large-scale company may want to use security level 3.|
|`depth`|Exponent that affects how many private key/address pairs Compass has. The total number of pairs depends on this formula: 2<sup>depth</sup>.|The greater the depth, the longer it takes to compute the Merkle tree, but the more bundles Compass can sign and send. The maximum depth you can use depends on the [`MAX_DEPTH` parameter](root://iri/1.0/references/iri-configuration-options.md#max-depth) of your node.|
|`mwm`|[minimum weight magnitude](root://getting-started/1.0/references/glossary.md#minimum-weight-magnitude)|The higher the MWM, the harder it is to do the proof of work for a transaction.|
|`tick`|Number of milliseconds Compass waits after creating a milestone|The longer the tick, the fewer transactions can be confirmed in your network, but the more uptime your network will have. The interval between milestones also depends on the length of time it takes Compass to create, sign and send a milestone bundle after the tick. |
|`host`|URL of the IOTA node to which Compass sends milestones||

