# Thermal ML notebooks

```sh
python -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
jupyter notebook
```

- **[train_voltages.ipynb](train_voltages.ipynb)** trains on your measured CSV and saves a checkpoint. Start here with lab data. Put one spectrum per row, followed by the applied voltages. Set `SPECTRUM_POINTS` to match the scan. Each voltage column gets one model output.
- **[dual_ring_training.ipynb](dual_ring_training.ipynb)** trains both CNNs on simulated coupled-ring spectra and compares transfer methods. The two outputs are ring frequencies in GHz.
- **[transfer_learning.ipynb](transfer_learning.ipynb)** runs the six-control independent-ring simulation and compares adaptation across two packages.

Run the notebooks from this folder. The two simulations generate their own data. A GPU helps for the transfer runs.
