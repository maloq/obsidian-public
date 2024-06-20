Revisiting the Common Neighbour Analysis
https://arxiv.org/abs/2003.08879

Classify each atom's local environment based on the type of structure (e.g., FCC, BCC, HCP, or amorphous).
Direct method and relatively straightforward to implement.

1. Compute a neighbor list for each atom using a cutoff radius (typically the first minimum of the RDF).
2. For each pair of neighboring atoms, determine the number of common neighbors they share.
3. Classify each atom based on the patterns of common neighbors. Atoms in crystalline structures will show distinct CNA signatures.