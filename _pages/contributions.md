---
layout: page
permalink: /contributions/
title: contributions
description: open-source contributions to scientific software projects
nav: true
nav_order: 4
---

<style>
.contrib-list {
  margin-top: 1.5rem;
}

.contrib-item {
  display: flex;
  gap: 1.2rem;
  padding: 1.2rem 0;
  border-bottom: 1px solid #ebebeb;
  align-items: flex-start;
}

.contrib-item:last-child {
  border-bottom: none;
}

.contrib-meta {
  min-width: 90px;
  text-align: right;
  flex-shrink: 0;
}

.contrib-date {
  font-size: 0.78rem;
  color: #888;
  font-family: monospace;
}

.contrib-status {
  display: inline-block;
  margin-top: 0.3rem;
  font-size: 0.65rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.06em;
  padding: 0.15rem 0.4rem;
  border-radius: 3px;
  background: #e8f5e9;
  color: #2e7d32;
  border: 1px solid #a5d6a7;
}

.contrib-body {
  flex: 1;
}

.contrib-title {
  font-size: 0.95rem;
  font-weight: 600;
  color: #1a1a1a;
  margin-bottom: 0.2rem;
  line-height: 1.3;
}

.contrib-title a {
  color: inherit;
  text-decoration: none;
}

.contrib-title a:hover {
  text-decoration: underline;
}

.contrib-repo {
  font-size: 0.78rem;
  color: #555;
  margin-bottom: 0.45rem;
}

.contrib-repo a {
  color: #555;
  text-decoration: none;
  font-family: monospace;
}

.contrib-repo a:hover {
  color: #1a1a1a;
  text-decoration: underline;
}

.contrib-company {
  display: inline-flex;
  align-items: center;
  gap: 0.25rem;
  font-size: 0.73rem;
  color: #666;
  text-decoration: none;
  margin-left: 0.5rem;
}

.contrib-company:hover {
  color: #333;
  text-decoration: underline;
}

.contrib-desc {
  font-size: 0.85rem;
  color: #444;
  line-height: 1.55;
  margin: 0;
}
</style>

<div class="contrib-list">

  <div class="contrib-item">
    <div class="contrib-meta">
      <div class="contrib-date">Jun 2026</div>
      <div class="contrib-status">merged</div>
    </div>
    <div class="contrib-body">
      <div class="contrib-title">
        <a href="https://github.com/rowansci/openconf/pull/5" target="_blank" rel="noopener noreferrer">
          Fix low-mode vibrational analysis to use mass-weighted coordinates
        </a>
      </div>
      <div class="contrib-repo">
        <a href="https://github.com/rowansci/openconf" target="_blank" rel="noopener noreferrer">rowansci/openconf</a>
        <a class="contrib-company" href="https://rowansci.com" target="_blank" rel="noopener noreferrer">
          <i class="fas fa-building" style="font-size: 0.65rem;"></i> Rowan Science
        </a>
      </div>
      <p class="contrib-desc">
        Corrected the GF-matrix vibrational analysis implementation to use mass-weighted Cartesian coordinates. 
        The prior code used unweighted coordinates, causing heavy atoms (Br, I, S) to artificially dominate 
        eigenvalue calculations and misidentify soft conformational modes. Fix substantially reranks low-frequency 
        modes in heavy-atom systems — e.g. 2-iodothiophene shifted from 3 to 5 correctly identified soft modes, 
        with iodine displacement dropping from 59% to ~3%.
      </p>
    </div>
  </div>

</div>
