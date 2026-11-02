# mdn-motor-decoding

Probabilistic decoding of future motor intent from cortical population activity with Mixture Density Networks (MDNs).

## Notebook

The main implementation is in `mdn_future_motor_intent.ipynb`.

It includes:

- Sliding-window PMd/M1 spike feature construction
- Future velocity prediction at configurable horizons
- Deterministic baseline decoder (MSE)
- Mixture Density Network decoder (mixture weights, means, and covariances)
- Deterministic metrics: RMSE, MAE, R²
- Probabilistic metrics: NLL, calibration, prediction interval coverage
