 Characterizing M-Dwarf Flare Impulsiveness Across the Convective Boundary

An automated, high-cadence computational pipeline designed to query, extract, and statistically analyze stellar flare morphologies across the M4V convective boundary using **NASA TESS (20-second cadence)** and **Gaia DR3** data.

##  Overview & Physical Motivation
This project investigates a fundamental transition in stellar astrophysics: **how the disappearance of the radiative core (at spectral type ~M4V) alters magnetic reconnection dynamics.** 

While partially convective stars (<M4V) generate structured magnetic fields via a shear-driven interface dynamo at the tachocline, fully convective stars (≥M4V) rely on chaotic, turbulent dynamos. By mapping the structural "fingerprint" of flare light curves—specifically the impulsiveness ratio (t rise /t total)—this study provides crucial, data-driven constraints on stellar magnetohydrodynamic (MHD) models and magnetic reconnection geometries.

##  Key Scientific Findings
Using a pipeline-derived dataset of **196 high-cadence stellar flares**, this study reveals a highly significant physical shift at the M4V boundary:
* **Mann-Whitney U Test ($p = 1.06 \times 10^{-8}$):** Conclusively proves that fully convective stars exhibit much higher (more symmetric) impulsiveness ratios. This points to a transition from single-loop reconnection to a  cascade of sympathetic, multi-loop reconnection events driven by turbulent dynamos.
* **Kolmogorov-Smirnov Test ($D = 0.3965, p = 4.54 \times 10^{-7}$):** Dismisses the null hypothesis that partially and fully convective flare profiles share the same distribution.
* **Anderson-Darling Test ($A^2 = 19.90, p < 0.001$):** Confirms profound differences in the extreme behavioral tails (outliers) of both populations.

 Repository Structure
* `/01_setup.ipynb` — Initial pipeline prototyping and parameter tuning.
* `/02_bulk_pipeline.ipynb` — Batch extraction loop utilizing `lightkurve` to query MAST, detrend, and isolate flares.
* `/03_statistical_analysis.ipynb` — Hypothesis testing (K-S, A-D, Mann-Whitney U) and scientific plotting.
* `/extracted_flares.csv` — The compiled dataset of 196 verified flares.
* `/flare_convective_cdf.pdf` — Generated cumulative distribution function plot.
* `/flare_systematic_scaling.pdf` — Subtype boxplot.
