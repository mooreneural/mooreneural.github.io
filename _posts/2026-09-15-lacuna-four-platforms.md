---
layout: post
title: "Lacuna now runs on four platforms"
date: 2026-09-15
source: linkedin
source_url: https://www.linkedin.com/feed/update/urn:li:ugcPost:7505286882034016256/
---
Lacuna is now usable across Anthropic's Claude Science, OpenAI's GPT-Rosalind, Tamarind Bio, and Neurosnap Inc.

Lacuna is the open-source cryptic pocket tool I built to find binding sites that are invisible in a protein's static structure and only appear as the protein moves.

Instead of searching one conformation, it generates or accepts a conformational ensemble, detects pockets across every state, and tracks the same sites as they open and close.

That matters because some of the most important drug targets do not present an obvious pocket in their ground state.

KRAS is the classic example. Its switch-II pocket was considered inaccessible for decades, yet that hidden site ultimately enabled drugs like sotorasib and adagrasib.

Lacuna recovered that same region on KRAS despite KRAS not appearing in the benchmark used to fit the model. The relevant sites appeared among the top-ranked predictions, with one pocket opening roughly nine-fold across the ensemble.

The latest version also combines the original cavity detector with a learned surface detector designed specifically to catch sites that have not formed a strong concavity yet.

On held-out CryptoBench data, that moves coverage from 68.5% to 86.4% and top-five recovery from 57.1% to 73.9%.

And now you do not have to run everything locally.

pip install lacuna-pockets

It is MIT licensed, CPU compatible, and open source.

If you use it on a target of your own, I would genuinely like to hear what it finds.
