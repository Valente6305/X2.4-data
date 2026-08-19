# AR 4419 X2.4 radio/LFF reproducibility deposit

This versioned deposit supports the fixed-seed PIKAIA searches and the
uncertainty-weight sensitivity statements in the associated manuscript. It is
deliberately limited to machine-readable configurations and derived numerical
outputs. Manuscript sources, credentials, workstation paths, proprietary or
licence-unclear legacy code, and third-party observational files are excluded.

## Contents

- `config/fixed_seed_searches.json`: seeds, objective, PIKAIA controls, model
  frequencies, flux targets, and complete broad parameter bounds.
- `outputs/independent_search_summary.csv`: best solution and profile range for
  each search.
- `outputs/evaluations_seed_*.csv`: all recorded evaluated models for each
  fixed seed, including the objective components.
- `outputs/objective_profile_models.csv`: models satisfying
  `Q <= Qmin + 2` within their own run.
- `outputs/field_profile_summary.txt`: combined field-profile summary.
- `outputs/flux_weight_sensitivity.csv`: re-scoring of the published seeded-fit
  fluxes under four uncertainty-weight schemes.
- `outputs/seeded_fit_fluxes.csv`: observed and model fluxes used in the
  sensitivity calculation.

The objective is `Q = 6 Q_spec + Q_6.77 + Q_9.69`. The objective-profile set is
a diagnostic, not a confidence or credible interval. The measured spectrum is
still rising at 17 GHz, and several retained models approach the 5 kG search
bound; consequently the deposit does not establish a unique magnetic field or
an upper confidence limit.

## Parameter conventions

`ie` is the dimensionless longitudinal nonthermal-electron density shape
parameter; `delta` is the nonthermal electron energy power-law index;
`logNe` and `logNp` are base-10 logarithms of number densities in cm^-3;
`As_pct` is field/dipole asymmetry in percent; `Az_deg` is loop azimuth;
`R_Rsun`, `FS_Rsun`, and `H_Rsun` are cross-section radius, footpoint
separation, and loop height in solar radii; `incl_deg` is loop inclination; and
`Bbase_G` is the loop-base field normalization in gauss.

## Observational products

The source observations remain available from their providers using the
identifiers reported in the article. Redistribution rights remain with those
providers. The numerical outputs here are sufficient to audit the reported
search summaries without redistributing those source products.
