---
title: "connectomes"
type: "[[Concept]]"
domain: "[[The Commons]]"
Lifestage: "🌱 Seed"
---

# Connectome
A **connectome** is essentially the complete “wiring diagram” of a nervous system—i.e. the map of all the neurons (or neural regions) and the connections between them.  In practice you’ll see it used in two main senses:

## Structural Connectome
A graph whose nodes are neurons (or brain regions) and whose edges are anatomical links (synapses, fiber tracts).  
Often reconstructed with techniques like electron‐microscopy (at the microscale) or tractography (at the macroscale).

## Functional Connectome
A network defined by statistical relationships—often correlations—between activity patterns in different regions (e.g. fMRI resting‐state networks).  
Captures which areas tend to fire together, suggesting functional coupling rather than direct anatomical links.

## Why it Matters:
  - Understanding how patterns of connectivity give rise to cognition, behavior, and consciousness.  
  - Identifying how diseases (Alzheimer’s, schizophrenia, autism) alter network topology—small‐worldness, hubs, modularity.  
  - Guiding brain‐machine interfaces and regenerative therapies by knowing which circuits do what.

## Graph‐theoretic View:
  If we label each node by an $index (i)$, the connectome can be encoded in an adjacency matrix  
  $$[
    A_{ij} = 
    \begin{cases}
      1, & \text{if node $i$ is connected to node $j$} \
      0, & \text{otherwise}
    \end{cases}
  ]
  $$
  (or in weighted form, $(A_{ij})$ carrying the strength or number of fibers).

**Major effort:** the Human Connectome Project, which uses high‐field MRI, MEG/EEG, and behavioral testing to chart the human brain’s large‐scale connectome—and make the data public for researchers worldwide.
