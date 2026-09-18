---
layout: about
title: about
permalink: /
subtitle: Ph.D. Student @ <a href='https://www.tamu.edu/'>Texas A&M University</a>.

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  address: >
    <p>Houston, TX</p>

news: false  # includes a list of news items
latest_posts: true  # includes a list of the newest posts
selected_papers: false # includes a list of papers marked as "selected={true}"
social: true  # includes social icons at the bottom of the page
---

Researcher working at the interface of neuroscience, natural products, and AI-driven drug discovery. My research focuses on computational modeling of neuroinflammation and neural plasticity, with an emphasis on identifying plant-derived and natural product-inspired compounds that may influence therapeutic pathways. I build in silico pipelines for molecular screening, receptor-state classification, and translational discovery workflows that connect computational biology with future wet-lab validation.

I am the author of <a href="https://github.com/mooreneural/lacuna">Lacuna</a>, an open-source tool for finding cryptic binding pockets that only appear as a protein moves. It is available on Claude Science, GPT-Rosalind, Tamarind Bio, and Neurosnap.

<style>
  .featured-box {
    border: 1px solid var(--global-divider-color);
    border-left: 3px solid var(--global-theme-color);
    border-radius: 4px;
    padding: 0.9rem 1.1rem;
    margin: 1.4rem 0 0.6rem 0;
  }
  .featured-label {
    font-size: 0.65rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.08em;
    color: var(--global-text-color-light);
    margin-bottom: 0.3rem;
  }
  .featured-title {
    font-size: 1.05rem;
    font-weight: 600;
    margin-bottom: 0.25rem;
  }
  .featured-title a {
    color: var(--global-text-color);
    text-decoration: none;
  }
  .featured-title a:hover {
    text-decoration: underline;
  }
  .featured-desc {
    font-size: 0.86rem;
    color: var(--global-text-color);
    line-height: 1.5;
    margin: 0 0 0.6rem 0;
  }
  .featured-links {
    display: flex;
    flex-wrap: wrap;
    gap: 0.3rem;
  }
  .featured-links a {
    font-size: 0.7rem;
    font-weight: 500;
    padding: 0.2rem 0.55rem;
    border-radius: 3px;
    border: 1.5px solid var(--global-divider-color);
    color: var(--global-text-color-light);
    text-decoration: none;
    transition: border-color 0.15s, color 0.15s;
  }
  .featured-links a:hover {
    border-color: var(--global-text-color);
    color: var(--global-text-color);
    text-decoration: none;
  }
</style>

<div class="featured-box">
  <div class="featured-label">Featured</div>
  <div class="featured-title"><a href="https://github.com/mooreneural/lacuna" target="_blank" rel="noopener noreferrer">Lacuna</a></div>
  <p class="featured-desc">Cryptic binding pocket discovery via conformational ensemble analysis. Generates an ensemble, detects pockets in every conformer, and clusters them to surface sites that are closed in the static structure. MIT licensed, runs on a CPU, and ships an MCP server and Claude skill.</p>
  <div class="featured-links">
    <a href="https://github.com/mooreneural/lacuna" target="_blank" rel="noopener noreferrer"><i class="fab fa-github" style="margin-right:4px;"></i>GitHub</a>
    <a href="https://www.biorxiv.org/content/10.64898/2026.08.14.744956v2" target="_blank" rel="noopener noreferrer"><i class="fas fa-file-alt" style="margin-right:4px;"></i>Preprint</a>
    <a href="https://pypi.org/project/lacuna-pockets/" target="_blank" rel="noopener noreferrer"><i class="fab fa-python" style="margin-right:4px;"></i>PyPI</a>
    <a href="https://app.tamarind.bio/tools/lacuna" target="_blank" rel="noopener noreferrer"><i class="fas fa-server" style="margin-right:4px;"></i>Run on Tamarind</a>
    <a href="https://neurosnap.ai/service/Lacuna%20Cryptic%20Pocket%20Discovery" target="_blank" rel="noopener noreferrer"><i class="fas fa-server" style="margin-right:4px;"></i>Run on Neurosnap</a>
  </div>
</div>
