# Project 02: Synthetic-Data LMM Exercise for Visual Word Recognition

## Overview

This repository contains a Python training exercise using synthetically generated reaction-time (RT) data. The simplified three-condition design is conceptually inspired by masked morphological priming research, including Beyersmann et al. (2012, 2016).

This project is not an empirical replication or reanalysis of either study. It does not use original participant data, experimental stimuli, or reported parameter estimates from the cited papers.

## What the Notebook Implements

The notebook:

- generates 3,600 synthetic observations for 40 simulated participants;
- assigns 30 condition-specific item labels to each of three conditions:
  `Morphological`, `Orthographic`, and `Unrelated`;
- sets illustrative condition effects of −40 ms, −10 ms, and 0 ms;
- adds simulated participant-level and item-level intercept variation and trial noise;
- removes RTs outside 300–1500 ms and observations beyond 2.5 within-participant standard deviations;
- visualizes the resulting RT distributions; and
- fits the following Linear Mixed-Effects Model using `statsmodels`:

`RT ~ C(Condition)`

The fitted model uses `Unrelated` as the reference condition and includes a random intercept for `Subject`. It estimates the fixed contrasts of `Orthographic` versus `Unrelated` and `Morphological` versus `Unrelated`.

## Model Scope and Limitations

- The fitted LMM includes a participant random intercept only.
- Although item-level variation is included during synthetic data generation and item identifiers are retained, the fitted model does not include an item random effect.
- Therefore, the current analysis is not a crossed subject-and-item random-effects model.
- The condition effects are specified in advance during data generation. Recovering significant differences therefore demonstrates model behavior under this simulation, not empirical evidence about human morphological processing.
- The notebook analyzes RT only; it does not analyze accuracy.
- The project does not reproduce the experimental procedure, stimuli, sample, or statistical analyses of the cited studies.

## Purpose

The repository documents introductory practice in:

- generating structured synthetic psycholinguistic data;
- preprocessing and visualizing RT distributions;
- fitting a basic mixed-effects model in Python; and
- interpreting fixed-effect contrasts while stating the model’s limitations.

## Technical Stack

- `pandas`
- `numpy`
- `statsmodels`
- `seaborn`
- `matplotlib`

## File

- `Beyersmann_LMM.ipynb` — synthetic-data generation, preprocessing, visualization, and LMM fitting

## Conceptual References

- Beyersmann, E., Castles, A., & Coltheart, M. (2012). Morphological processing during visual word recognition in developing readers: Evidence from masked priming. *The Quarterly Journal of Experimental Psychology, 65*(7), 1306–1326. https://doi.org/10.1080/17470218.2012.656661
- Beyersmann, E., Ziegler, J. C., Castles, A., Coltheart, M., Kezilas, Y., & Grainger, J. (2016). Morpho-orthographic segmentation without semantics. *Psychonomic Bulletin & Review, 23*(2), 533–539. https://doi.org/10.3758/s13423-015-0927-z