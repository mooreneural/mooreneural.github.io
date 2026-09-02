---
layout: post
title: "How do you drug a protein that has no pocket?"
date: 2026-09-02
source: linkedin
source_url: https://www.linkedin.com/posts/claynovel_how-do-you-drug-a-protein-that-has-no-pocket-share-7501033877751255040-DKGP/
---
Many disease-relevant targets are called undruggable not because they are biologically intractable, but because no binding site is visible in their ground state.

K-Ras was considered undruggable for thirty years, until a cryptic pocket was found beneath its switch-II region. That pocket now backs sotorasib and adagrasib.

Structure predictors return one static conformation, and most pocket finders search exactly that snapshot. A site that is closed in it does not exist to them.

Lacuna does not stop at the static structure. It generates a conformational ensemble from your input, detects cavities in every conformer, and clusters them across the ensemble to surface sites that appear only transiently.

It is open source under MIT, and it runs on a CPU. A 456-residue dimer takes under 3 seconds on a laptop with no GPU.

pip install lacuna-pockets

Lacuna stands on other people's work. Ensembles come from OpenMM for implicit solvent MD, Boltz for diffusion sampling, and an ANM implementation for normal modes. Ranking optionally uses ESM-2. Benchmarking is against CryptoBench, with fpocket, P2Rank, IF-SitePred and MDpocket as comparisons.
