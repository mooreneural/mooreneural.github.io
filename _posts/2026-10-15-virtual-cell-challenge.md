---
layout: post
title: "Competing in the 2026 Virtual Cell Challenge"
date: 2026-10-15
source: linkedin
source_url: https://www.linkedin.com/posts/mooreneural_virtualcellchallenge-aiforbiology-computationalbiology-ugcPost-7516685653074640896-tb2R/
---
Can a model predict an experiment that has never been run, in a cell type it has never seen perturbed?

That is the question behind the Arc Institute's 2026 Virtual Cell Challenge, and it is the problem I have been working on.

The setup is strict. A model gets the unperturbed state of a cell line and the gene to be knocked down with CRISPRi, and it has to predict how thousands of genes respond. It sees no perturbation data from that cellular context: fully zero-shot. Its predictions are then scored against Perturb-seq measurements it has never seen.

My approach is intentionally constrained: one person, one desktop GPU, and only openly licensed data. I want to find out how far a carefully built approach can go against systems trained on much larger private datasets with far more compute. I am close to a hundred model iterations in, and I plan to release my code and my negative results after the challenge closes.

The problem connects to my other work. Lacuna, my structural biology tool, looks for binding pockets that appear only transiently and are invisible in any single static structure. Here the hidden information is a cell's response to a perturbation it has never experienced, inferred from how related contexts behave.

Arc included me in their showcase of this year's competitors. With more than 1,500 teams on the leaderboard, the range of backgrounds and ideas is one of the best parts of this challenge, and the other profiles are worth reading: [https://arcinstitute.org/news/vcc-competitor-showcase-2026](https://arcinstitute.org/news/vcc-competitor-showcase-2026)

Thank you to Arc Institute for building such an ambitious open benchmark, and to NVIDIA, 10x Genomics and Ultima Genomics for supporting it.

The final round, on held-out contexts no one has seen, starts in 7 days.
