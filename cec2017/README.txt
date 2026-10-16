CEC2017: reported benchmark summaries

Scope
This folder contains the study's reported numerical summaries for the 15
50-dimensional CEC2017 functions used in Tables III and IV of
"DDCPO: A Dimension-Decoupled Crested Porcupine Optimizer for Mobile Robot
Path Planning". It is a data-only export, not an implementation or a complete
archive of the underlying independent runs.

Functions, in manuscript order:
F1, F6, F7, F12, F13, F14, F15, F23, F24, F25, F26, F27, F28, F29, F30.

Algorithms, in manuscript order:
DDCPO, CPO, AO, DBO, PSO, WOA, SSA.

Files
- cec2017_reported_summary.csv:
  105 records, one function-algorithm pair per row. Values are the reported
  Best, Avg, Worst, and Std. entries from Table III. Dimension is 50 and
  reported_independent_runs is 30, as stated in the manuscript.
- cec2017_reported_pairwise.csv:
  90 records, one function-comparison pair per row, copied from Table IV.
  DDCPO is the reference algorithm; the other six algorithms are the
  comparison algorithms.
- cec2017_reported_pairwise_counts.csv:
  Six records copied from the final win/loss/tie row of Table IV.
- SOURCES.csv:
  Source names, manuscript locators, and SHA-256 identifiers for this export.

Field meanings
The manuscript defines objective error as abs(f(x_best) - f_opt).
best_objective_error, mean_objective_error, worst_objective_error, and
sample_std_objective_error reproduce the minimum, arithmetic mean, maximum,
and sample standard deviation reported across the 30 independent runs.
They are summaries, not per-run observations.

reported_p_value and reported_decision_symbol reproduce the manuscript's
Wilcoxon rank-sum comparison results. Under the paper's convention, for
p < 0.05, '+' denotes a lower reported mean for DDCPO and '-' denotes a
higher reported mean; '=' denotes p >= 0.05. Symbols and counts were copied,
not recalculated. The columns called reported_wins/losses/ties reproduce
that convention and do not constitute a new statistical analysis.

Precision and extraction
Every reported numerical string, including its scientific notation and
displayed precision, was preserved from the final manuscript tables.
The extraction performs no averaging, rounding, statistical tests, curve
digitization, or optimization. No additional precision should be inferred.

Availability limits
The archive inspected for this release did not provide complete numeric
per-run CEC samples or convergence trajectories for all 15 functions.
The available archival provenance for Figures 3 and 4 describes raster
layers taken from original plot images and explicitly states that raw
trajectories and trial samples were unavailable. Those images are not
numeric source series; no values were inferred from their pixels.
Consequently, these CSVs cannot reproduce the boxplots or convergence
curves from raw numerical observations.

Excluded materials
No algorithm or plotting code, executables, third-party CEC evaluation
implementations, official shift/rotation/shuffle input files, original
plot images, manuscript files, author contact information, or unpublished
per-run data are included.

External benchmark
The CEC2017 benchmark definitions and official evaluation/input package
must be obtained separately from the original CEC2017 benchmark source
associated with:
N. H. Awad, M. Z. Ali, J. J. Liang, B. Y. Qu, and P. N. Suganthan,
"Problem Definitions and Evaluation Criteria for the CEC 2017 Special
Session and Competition on Single Objective Bound Constrained
Real-Parameter Numerical Optimization," Technical Report,
Nanyang Technological University, Singapore, 2016.
This release does not redistribute that third-party package.
