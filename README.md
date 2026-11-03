# mdn-motor-decoding

Probabilistic decoding of future motor intent from cortical population activity with Mixture Density Networks (MDNs).

## Setup with Miniconda or Anaconda

The recommended setup uses the Conda environment described in [environment.yml](environment.yml). From the repository directory (`mdn-motor-decoding`), open Anaconda Prompt or a new VS Code PowerShell terminal and run:

```text
conda env create -f environment.yml
conda activate mdn-motor-decoding
python -m ipykernel install --user --name mdn-motor-decoding --display-name "Python (MDN Motor Decoding)"
```

If the environment already exists and the YAML file has changed, update it with:

```text
conda env update -f environment.yml --prune
```

In VS Code, open `mdn_future_motor_intent.ipynb`, select the `Python (MDN Motor Decoding)` kernel, and run the notebook cells from top to bottom.

To leave the Conda environment:

```text
conda deactivate
```

To remove the environment completely:

```text
conda env remove --name mdn-motor-decoding
```

## Notebook

The main implementation is in `mdn_future_motor_intent.ipynb`.

It includes:

- Sliding-window PMd/M1 spike feature construction
- Future velocity prediction at configurable horizons
- Deterministic baseline decoder (MSE)
- Mixture Density Network decoder (mixture weights, means, and covariances)
- Deterministic metrics: RMSE, MAE, R²
- Probabilistic metrics: NLL, calibration, prediction interval coverage
