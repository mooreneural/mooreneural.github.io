---
layout: post
title: "Lacuna is now runnable in Horus"
date: 2026-10-07
source: linkedin
source_url: https://www.linkedin.com/feed/update/urn:li:activity:7511419442493521921/
---
Lacuna is now runnable in Horus, Temple Compute's workflow platform, as a ready-to-run workflow built by Christian Domínguez Dalmases, CEO and CTO of Temple Compute.

Most binding-pocket tools only find a pocket where the surface is already concave. Cryptic pockets are the ones that stay hidden in the apo structure and only open when a ligand binds. Lacuna generates a conformational ensemble, detects pockets in every conformer, clusters them across the ensemble, and ranks what survives.

The Horus workflow needs no installation steps or manual wiring. It produces an interactive HTML report with a sortable, filterable pocket table and a live 3D view, where clicking View on any row jumps to that pocket's lining residues. It also writes a CSV of every pocket's scores, ready for downstream analysis.

A second variant goes further: it docks a ligand library into the top-ranked pocket with AutoDock Vina, one run per ligand in parallel, and ends in a ranked binding-affinity table.

The example is apo KRAS(G12C), the textbook case: the switch-II pocket isn't there until an inhibitor binds, and Lacuna surfaces it from the unbound structure.

Try it: [Lacuna Cryptic Pocket Discovery on Horus](https://os.templecompute.com/library?release=lacuna-cryptic-pocket-discovery-d2087c)
