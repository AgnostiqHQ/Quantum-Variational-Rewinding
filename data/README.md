# Data sets

This folder contains the all of the cryptocurrency time series data used in the main article for ``Quantum Variational Rewinding for Time Series Anomaly Detection".

There are two folders:

## large_data_sets

Contains all of the time series retrieved from Binance as described in the supplemental material in the main article. \*\_dirty\_\* file names correspong to data sets capped with a $~$ in the main article. \*\_clean\_\* means are those data sets without the cap.

## separated_data

Contains the smaller time series data sets used in the main article. These are the sets used for the IBM quantum computer runs.

All data has been re-scaled in the way indicated in the supplemental material of the article. The format is `pickle` and can be loaded like below:

```python
import pickle

clean_btc_open = pickle.load(open("../../data/boc_data/quantum_ready/diff_scale/open_clean_btc.pickle", "rb"))
```
which would contain the mean deviation of the open price in the presence of large transactions of BTC on the blockchain.
