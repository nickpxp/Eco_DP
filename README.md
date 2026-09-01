# Eco_DP
The Energy Cost of Verifying a Privacy Defense

Four membership inference audits
(loss-threshold, RMIA, LiRA, one-run canary) run against a 12-lead ECG
classifier trained on PTB-XL with DP-SGD, with the energy of every step metered.

## Files

- `paper_utils_dpcnn.py` — InceptionTime1D with GroupNorm, DP-SGD via Opacus,
  RDP accountant, class weighting, PTB-XL loading, checkpoint I/O
- `run_full_sweep.py` — trains the 33 targets and the shadow pool, runs
  loss-threshold, RMIA and LiRA, meters energy via NVML and RAPL
- `run_canary_audit.py` — the one-run canary audit

## Data

PTB-XL is public: https://physionet.org/content/ptb-xl/

