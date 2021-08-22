---
layout: project
title: Cache
subtitle: Implementation of a DM Cache and a 4-way SA Cache
---

Implementation of a [Direct Mapped Cache](https://en.wikipedia.org/wiki/Cache_placement_policies#Direct-mapped_cache) and a 4-way [Set Associative Cache](https://en.wikipedia.org/wiki/Cache_placement_policies#Set-associative_cache) in python.

#### Hit rates and miss rates of the two caches for five input memory trace files:

<img src="https://raw.githubusercontent.com/shrey27tri01/Cache-python/master/rates.png">

**Note**: The LRU (Least Recently Used) policy has been used for replacement in the 4-way Set Associative Cache.

#### Observations:

- Hit rates for the Set Associative Cache are slightly greater than the those for the Direct Mapped Cache.
- Consequently, miss rates for the Set Associative Cache are slightly less than those for the Direct Mapped Cache, for all of the five memory trace files.
- These observations confirm to our prediction that the Set Associative Cache is a better cache, considering the "spatial locality" of memory.

#### Implementation:

[GitHub Repository](https://github.com/shrey27tri01/Cache-python)




