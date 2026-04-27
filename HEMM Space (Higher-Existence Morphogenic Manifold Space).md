# HEMM Space
A **HEMM Space** is a two-by-three array of subspaces, each of which is itself a two-by-three matrix of elemental coordinates. One of these subspaces (here chosen as $(M_{22})$) carries the **Cosmic Index Factor** ([[CIF (Cosmic Index Factor)]]), enabling universe-scale calibrations. 
## 1. Block Structure
We organize HEMM as: 
$$[ \mathrm{HEMM}  =  \begin{pmatrix} M_{11} & M_{12} & M_{13} \\ M_{21} & M_{22} & M_{23} \end{pmatrix}, ]$$ where each block $(M_{ij}) is a (2\times3)$ matrix of base elements $$(a_{kl}^{(ij)}):  [ M_{ij} = \begin{pmatrix} a_{11}^{(ij)} & a_{12}^{(ij)} & a_{13}^{(ij)} \\ a_{21}^{(ij)} & a_{22}^{(ij)} & a_{23}^{(ij)} \end{pmatrix}, \quad i\in\{1,2\},\; j\in\{1,2,3\}. ]$$  
### 1.1 The CIF‐Bearing Subspace
By convention, the central block $(M_{22})$ is endowed with the Cosmic Index Factor:  $$[ M_{22} \;\xrightarrow{\;\text{CIF}\;}\; M_{22}^{(\mathrm{cif})}, ]$$  
linking the local HEMM coordinates to the global cosmic scale via the [[CIF (Cosmic Index Factor)|Cosmic Index Format (CIF)]] definition.  
## 2. LaTeX Representation
 $$ \mathrm{HEMM} = \begin{pmatrix} M_{11} & M_{12} & M_{13} \\ M_{21} & M_{22} & M_{23} \end{pmatrix}, \quad M_{ij} = \begin{pmatrix} a_{11}^{(ij)} & a_{12}^{(ij)} & a_{13}^{(ij)} \\ a_{21}^{(ij)} & a_{22}^{(ij)} & a_{23}^{(ij)} \end{pmatrix}. $$`

And the CIF‐tagged block:

$$ M_{22}^{(\mathrm{cif})} = \mathrm{CIF}\;\times\; \begin{pmatrix} a_{11}^{(22)} & a_{12}^{(22)} & a_{13}^{(22)} \\ a_{21}^{(22)} & a_{22}^{(22)} & a_{23}^{(22)} \end{pmatrix}. $$`

## 3. Conceptual Notes

- Each $(a_{kl}^{(ij)})$ can represent a coordinate axis, physical parameter, or “mode” in that subspace.
- The CIF rescales all entries in $(M_{22})$ to align local physics with the **Cosmic Index Frame**.
- You can choose any other $(M_{ij})$ for CIF or even support multiple CIF‐bearing blocks for more exotic geometries.
