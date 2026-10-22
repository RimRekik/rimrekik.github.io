---
title: "PepH-GAT: A hierarchical graph attention network for predicting peptide fragmentation spectra"
collection: publications
date: 2026-10-01
venue: 'In preparation'
status: 'In preparation'
excerpt: "<img src='/images/peptide-graph-abstract.png' width='520'><br/>Predicting peptide fragmentation spectra from hierarchical molecular graphs (atoms and amino acids)."
citation: '<b>R. Rekik</b>, L. Schneider, S. Derrode, Z. Bouyahia. &quot;PepH-GAT: A hierarchical graph attention network for predicting peptide fragmentation spectra.&quot; In preparation.'
---

<img src="/images/peptide-graph-abstract.png" alt="From peptide sequence to molecular structure, hierarchical atom–residue graph and predicted spectrum" width="100%">

*Graphical abstract: the peptide sequence is converted into its molecular structure, encoded as a hierarchical graph of atoms and amino-acid residues, and a hierarchical graph attention network predicts its fragmentation spectrum (observed spectrum in blue, prediction in red).*

**Status:** paper in preparation.

## Summary
Predicting the fragmentation spectrum of a peptide is central to protein identification in mass-spectrometry proteomics, and it is especially hard for chemically modified peptides. We represent each peptide at the molecular level, as a hierarchical graph that links atoms to amino-acid residues, and predict its spectrum with a hierarchical graph attention network. This molecular representation lets the model handle modifications it has rarely seen. Models are evaluated against experimentally measured spectra.
