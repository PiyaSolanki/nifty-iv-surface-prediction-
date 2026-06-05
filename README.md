# NIFTY Options IV Surface Reconstruction

## Competition
Finance Club, IIT Roorkee — Open Projects 2026

## Problem
Predict missing implied volatility values across strikes and timestamps 
for NIFTY50 weekly options chain data.

## Approach
- Cross-sectional PCHIP spline for interior cells (monotone-preserving interpolation)
- Linear extrapolation for boundary strikes
- Regime-aware evaluation separating expiry-day from non-expiry behaviour
- LightGBM with 18 features including DTE (time to maturity) as conditional model
- Temporal anchor blending for expiry-day cells

## Validation MSE
0.00017545 (walk-forward validation)

## Files
- `iv_surface_prediction.ipynb` — Main notebook (reproduces submission CSV exactly)
