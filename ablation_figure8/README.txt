DDCPO - data supporting the final Figure 8
==========================================

Scope
-----
This folder contains only existing numerical records used for the final mean
final-fitness rank figure and its 97.5% bootstrap confidence intervals.
The four manuscript labels are DDCPO, DDCPO-I, DDCPO-W, and DDCPO-S.
There are five map sizes (20, 30, 40, 50, and 60), with 30 matched trials per map:
150 map-seed trials and 600 group-run records in total.

Files
-----
figure8_matched_runs.csv
  Selected columns from the existing final rank-summary raw CSV. Row order and
  the selected source values are preserved. A matched trial is identified by
  (MapSize, RunIndex, Seed), and contains exactly one record for each group.

  MapSize: square grid side length, in cells.
  Variant: one of the four manuscript group labels.
  RunIndex: recorded trial index within a map.
  Seed: recorded random seed.
  BestScore: recorded final objective value, including any applicable penalty.
  Success: recorded success flag (1 = success; 0 = unsuccessful).
  EvaluationCount: recorded number of fitness evaluations.
  FinalFitnessRank: already-recorded within-trial rank of final fitness.
    Ranks were copied, not recomputed. Lower fitness receives the better rank;
    ties use the rank rule documented in figure8_methods.json.

figure8_plot_values.csv
  The four already-recorded plotted mean ranks and confidence-interval bounds.
  Decimal text is preserved from the final publication-figure metadata.
  Variant: group label.
  MeanFinalFitnessRank: plotted aggregate mean rank.
  CI_Lower / CI_Upper: plotted bootstrap confidence-interval endpoints.
  CIConfidenceLevel: 0.975 (97.5%).
  These are the existing plotted endpoints, not newly generated intervals.

figure8_methods.json
  Group definitions and the existing rank/bootstrap settings: 20,000 fitness
  evaluations per run; 5,000 bootstrap repetitions; resampling of complete
  matched four-group trials within each map; equal averaging of five map means.
  See this JSON for the original tie rule, bootstrap seed, and quantile rule.

Group definitions
-----------------
DDCPO: complete configuration.
DDCPO-I: uniform random initialization replaces hybrid Chebyshev-Tent
  initialization.
DDCPO-W: constant weight 0.75 replaces the nonlinear oscillatory search weight.
DDCPO-S: stagnation-triggered dimension-decoupled perturbation is disabled.

Preparation and coverage
------------------------
Values were selected from the existing Figure_8_rank_metadata.json and its
frozen Joint_ablation_rank_summary data. Unsuccessful runs and their recorded
penalties were retained. Only column selection and value-preserving file
serialization were performed for this release; no experiments, ranking, or
bootstrap calculations were rerun.

This folder contains no software, development searches, auxiliary comparison
groups, convergence histories, other ablation figures, logs, or older versions.
