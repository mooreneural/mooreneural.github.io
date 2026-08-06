---
layout: post
title: "Contributing to Nesso-1"
date: 2026-08-05
source: linkedin
source_url: https://www.linkedin.com/posts/claynovel_drugdiscovery-machinelearning-computationalbiology-share-7490807218221731840-oqXP/
---
I'm glad to be contributing to Recursion's Nesso-1 through PR #3. I identified two training-only tensors - `disto_target` and `token_to_rep_atom` - that were still being generated and transferred during inference even though Nesso-1's forward pass never used them.

Removing those unused inference tensors cut input-batch GPU memory from 155.1 MiB to 16.8 MiB, about 9x smaller, and reduced host-to-device transfer time from roughly 9.8 ms to 1.3 ms per batch, about 7x faster. The `disto_target` tensor alone accounted for exactly 64 MiB at N=512 and 144 MiB at N=768, all of which is now eliminated during inference. Featurization also improved by roughly 1.3–1.6x per record, while model outputs remained bit-identical.

Valence Labs and Recursion just released Nesso-1, a protein–ligand co-folding model for binding affinity prediction that runs approximately 10–20x faster than Boltz-2, enabling screening of significantly more compounds at the same computational cost.

Congratulations to Nikhil Shenoy, David Errington, Francesco Di Giovanni, Therence Bois, and everyone across Valence Labs and Recursion who helped bring Nesso-1 to life. Excited to see where the project goes next.
