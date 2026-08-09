# Project 02: Synthetic RT LMM Exercise for Visual Word Recognition

## Scope at a Glance

This repository contains an introductory Python exercise using synthetically generated reaction-time (RT) observations. Its three condition labels are conceptually inspired by masked morphological-priming research, including Beyersmann et al. (2012, 2016).

This is **not** an empirical replication or reanalysis. It does not use human data, original stimuli, reported parameter estimates, a masking procedure, lexical-decision responses, or accuracy data.

## What the Notebook Implements

The notebook:

- generates 3,600 synthetic observations for 40 synthetic participant IDs;
- assigns 30 condition-specific synthetic item IDs to each of three labels: `Morphological`, `Orthographic`, and `Unrelated`;
- prespecifies illustrative condition offsets of -40 ms, -10 ms, and 0 ms;
- adds participant-level intercept variation, item-level intercept variation, and residual noise;
- applies illustrative RT filtering choices;
- visualizes the resulting synthetic RT distributions; and
- fits `RT ~ C(Condition)` with a random intercept for `Subject` using `statsmodels`.

## Model Scope and Limitations

- The fitted LMM includes a participant random intercept only.
- Item-level variation is generated, but the fitted model omits an item random effect.
- The current analysis is therefore **not a crossed subject-item random-effects model**.
- Standard errors, confidence intervals, and p-values do not account for item-level clustering.
- The fitted coefficients are compared descriptively with the prespecified offsets in one simulated dataset. This is not a formal parameter-recovery study.
- Statistical significance is not treated as successful recovery and is not empirical evidence of priming in human readers.
- The project does not reproduce the participants, materials, procedure, or analyses of the cited studies.

## Purpose

The repository documents foundational practice in:

- generating structured synthetic observations;
- preprocessing and visualizing RT distributions;
- fitting a basic participant random-intercept LMM in Python; and
- interpreting fixed-effect contrasts while stating model limitations.

## Technical Stack

- `pandas`
- `numpy`
- `statsmodels`
- `seaborn`
- `matplotlib`

## File

- `Beyersmann_LMM.ipynb` - synthetic-data generation, illustrative preprocessing, visualization, and participant random-intercept LMM fitting

## Conceptual References

- Beyersmann, E., Castles, A., & Coltheart, M. (2012). Morphological processing during visual word recognition in developing readers: Evidence from masked priming. *The Quarterly Journal of Experimental Psychology, 65*(7), 1306-1326. https://doi.org/10.1080/17470218.2012.656661
- Beyersmann, E., Ziegler, J. C., Castles, A., Coltheart, M., Kezilas, Y., & Grainger, J. (2016). Morpho-orthographic segmentation without semantics. *Psychonomic Bulletin & Review, 23*(2), 533-539. https://doi.org/10.3758/s13423-015-0927-z

The cited studies provide conceptual background for the condition labels only. All numerical values and variance components in the notebook are manually selected for illustration.