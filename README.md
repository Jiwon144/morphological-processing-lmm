# [Project 02] Replication of Linear Mixed-Effects Models (LMM) in Visual Word Recognition
# morphological-processing-lmm

Python replication of Beyersmann et al. (2012, 2016) on masked morphological priming. Built to apply Linear Mixed-Effects Models (LMM) in psycholinguistics.

### About This Project

This project was driven by a profound interest in **psycholinguistics, specifically morphological processing and visual word recognition**. 

To deepen my understanding of these cognitive mechanisms, I chose to computationally replicate the core experimental paradigms from two seminal papers: **Beyersmann et al. (2012)** and **Beyersmann et al. (2016)**.

A primary methodological motivation for this repository was to independently implement **Linear Mixed-Effects Models (LMM)** in Python. By simulating the Masked Priming Lexical Decision Task, this pipeline demonstrates how to rigorously control for crossed random effects (Subjects and Items)—reflecting the current statistical gold standard in modern cognitive science.

### Methodological Note: Parametric Simulation for LMM Verification

The reaction time (RT) and accuracy datasets visualised and modeled in this repository are **synthetically simulated** based on the empirical parameters and behavioral effect sizes published by **Beyersmann et al. (2012, 2016)**.

In psycholinguistic methodological training, parametric data simulation serves as a standard benchmark to verify statistical modeling capabilities. The primary objectives of this simulation are:
1. **Model Specification:** To demonstrate the technical capability to specify and execute **Linear Mixed-Effects Models (LMM)** in Python (`statsmodels`), moving beyond traditional repeated-measures ANOVA.
2. **Random Effects Control:** To programmatically verify the correct handling of crossed random effects (Subjects and Items)—a critical statistical gold standard in visual word recognition and masked morphological priming research.

**References (Target Paradigms):**
* Beyersmann, E., Castles, A., & Coltheart, M. (2012). Morphological processing during visual word recognition in developing readers: Evidence from masked priming. *The Quarterly Journal of Experimental Psychology*, 65(7), 1306-1326.
* Beyersmann, E., Ziegler, J. C., Castles, A., Coltheart, M., Kezilas, Y., & Grainger, J. (2016). Morpho-orthographic segmentation without semantics. *Psychonomic Bulletin & Review*, 23(2), 533-539.
