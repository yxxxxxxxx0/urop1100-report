# From Daily Maximum-Temperature Forecasts to Calibrated Temperature-Bracket Probabilities: Evidence from Hong Kong and Shenzhen

UROP1100 final report, HKUST, summer 2026. Author: Cheng Shing Chi Justin.

**[Read the report (PDF)](UROP1100_Final_Report_Cheng_Shing_Chi_Justin.pdf)**

## Summary

Daily maximum-temperature forecasts for Hong Kong and Shenzhen are evaluated both as point predictions and as probability distributions over one-degree brackets.

- **Data:** 45,967 forecast records from ECMWF, GFS and ICON (1–7 day horizons, January 2022 to July 2026), matched with observed maxima from the Hong Kong Observatory and Shenzhen Bao'an Airport (ZGSZ).
- **Methods:** chronological evaluation of raw forecasts, rolling-bias correction, ARIMA/ARIMAX, tree-based models, LSTMs and probabilistic post-processing (NGBoost), scored with proper scoring rules. Confidence intervals use a 14-day block bootstrap to preserve temporal dependence.
- **Results:** Random Forest reduced test MAE from 1.724 °C to 1.170 °C (−32.1%). NGBoost with a Laplace distribution achieved bracket log loss 1.581, Brier score 0.755 and CRPS 0.856 °C.
- **Limitations:** calibration remained incomplete (top-bracket accuracy 34.0%; recalibration did not hold out of sample), and some archived forecast publication times cannot be verified. These are retrospective results; prospective timestamped data and an untouched test period are needed.
