# \# **AlphaFold2-guided de novo mini-protein design**



 *## **Overview***



This repository documents a small independent project exploring a proof-of-concept workflow in de novo protein design. A novel 66-residue sequence was engineered and evaluated using AlphaFold2 via ColabFold to test whether a rationally designed scaffold could adopt a stable fold and support a candidate catalytic site. The project uses structure prediction as a practical tool for assessing early-stage sequence design.



\## ***Designed sequences***



Two closely related sequences were examined.



***Novel sequence***





"ALEKKEKLLEMLKEAMKEKAMELEKKMKEMMKMMEEAEEMMMEMMMLMEAMEMKLKALKL"





***Mutated variant***





"ALEKKEKLLEMLKEAMKEKAMELEKKMKEMMKMMSEAEEMMMEMMMLHEAMEMKDKALKL"





FASTA files are available in the `sequences/` directory.



\## ***Method (ColabFold workflow)***



Structure prediction was performed using ColabFold (AlphaFold2 implementation on Google Colab):



1\. Input sequences were submitted as FASTA files to ColabFold.

2\. Default AlphaFold2 settings were used for structure prediction.

3\. The top-ranked model was selected based on confidence scores.

4\. Structural inspection and pocket analysis were carried out in PyMOL.

5\. Structural variants were compared using RMSD-based alignment.



\## ***Results***



AlphaFold2 predicted a compact α-helical scaffold with high overall confidence (mean pLDDT ≈ 94). The engineered residues (S35–H48–D55) form a spatially clustered, solvent-accessible groove consistent with a plausible binding pocket. Structural alignment between sequence variants shows preservation of the overall fold, suggesting stability of the designed scaffold



\## ***Conclusion***



The results indicate that a de novo sequence can be rationally engineered into a foldable scaffold with a geometrically plausible catalytic pocket. While functional activity remains to be validated through docking or molecular dynamics simulations, this work demonstrates how AlphaFold2 can be used to evaluate early-stage inverse protein design.



***## Future work***



Planned extensions include systematic sequence variant generation, docking against model ligands, and short molecular dynamics simulations to assess pocket stability.




