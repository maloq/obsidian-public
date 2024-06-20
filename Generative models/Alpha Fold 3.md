Abramson, J. _et al._ Accurate structure prediction of biomolecular interactions with AlphaFold 3. _Nature_ 1–3 (2024) doi:10.1038/s41586-024-07487-w.

The paper discusses the development of AlphaFold 3 (AF3), a model designed for high-accuracy prediction of biomolecular complex structures, including proteins, nucleic acids, and ligands. The major innovation in AF3 is its architecture, which simplifies multiple sequence alignment (MSA) processing and employs a diffusion module for direct prediction of raw atomic coordinates.

### Local Structure Topology

The section on local structure topology is covered under the discussion of the Diffusion Module and its operation:

1. **Diffusion Module**:
    
    - The Diffusion Module operates directly on raw atom coordinates and an abstract token representation.
    - Unlike AlphaFold 2, which used rotational frames and equivariant processing, AF3 simplifies this approach.
    - The module is trained to predict true atomic coordinates from "noised" ones. This denoising task at different noise levels allows the network to learn protein structures at various scales:
        - **Low Noise**: Emphasizes very local stereochemistry, ensuring sharp local structure details like side chain bond geometry.
        - **High Noise**: Focuses on large-scale structural aspects of the system.
    - This generative training approach results in a distribution of possible structures, with well-defined local structures even under uncertainty.
2. **Advantages**:
    
    - The generative nature avoids the need for torsion-based parametrizations and violation losses, making the model versatile for different chemical components.
    - It simplifies the machine learning architecture by not requiring global rotational and translational invariance or equivariance.
    - 
1. **Challenges**:
    
    - Generative models can hallucinate plausible-looking but incorrect structures in unstructured regions.
    - To mitigate this, a novel cross-distillation method enriches training data with predicted structures from AlphaFold-Multimer v2, which represents unstructured regions more realistically.
    - A diffusion "rollout" procedure is used during training to predict full structures and compute performance metrics for training the confidence head, addressing confidence measures in final predictions.
