---
layout: post
title: "Lacuna is now a skill in Claude Science"
date: 2026-09-09
source: linkedin
source_url: https://www.linkedin.com/posts/claynovel_drugdiscovery-computationalbiology-claude-share-7503217521651552256-KrYp/
---
Lacuna, the open-source cryptic pocket tool I built, is now importable as a skill in Anthropic's Claude Science. It finds cryptic binding pockets: sites that look closed or shallow in an unbound structure and only open when something binds. It generates a conformational ensemble, detects pockets in every conformer, and clusters them so a site that appears in only a few frames still gets reported, with a score for how much it opens relative to your input. Point Claude Science at mooreneural/lacuna under Skills, Import from GitHub. Then ask it for cryptic pockets on a structure and it handles the rest.

To check it does something real, I ran it on the KRAS switch II pocket. That site is absent from apo structures and only forms on covalent inhibitor binding, and KRAS appears nowhere in the benchmark Lacuna's models were fitted on, so neither the ranker nor the surface model has seen it. It came back twice, at ranks 4 and 6 of ten. Rank 4 is the compact switch II groove, His95 and Tyr96 plus the P-loop position that carries the G12C cysteine, 4.2 angstroms from where sotorasib sits. Rank 6 has the wider overlap, 11 of the 21 contact residues, with pocket atoms 1.5 angstroms from the nearest ligand atom, and it opens nine-fold across the ensemble. Everything ranked above them is the GDP site, which is a real pocket with a real ligand in it. On a protein the models have never seen.

1.1.0 also adds a learned surface detector. The original detector only proposes where there is already a concavity, which is exactly the wrong assumption for a cryptic site. Pooling both takes held-out coverage on CryptoBench from 68.5% to 86.4% and top-five recovery from 57.1% to 73.9%.

pip install lacuna-pockets
