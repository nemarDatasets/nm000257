# Imagined speech EEG dataset — short words condition (Nguyen et al. 2017)

## Overview

This dataset comprises preprocessed EEG recordings from 6 healthy participants performing imagined speech tasks with three short word conditions (out, in, up). The study employed a motor imagery paradigm with auditory and visual cueing, yielding 5,400 trials analyzed using Riemannian manifold methods and relevance vector machines for brain-computer interface applications.

## Dataset Summary

| Property | Value |
|---|---|
| Subjects | 6 |
| Channels | 64 |
| Classes | 3 |
| Trial length | 5 s |
| Sampling frequency | 256 Hz |
| Sessions | 1 |
| Total trials | 1800 |
| Paradigm | MotorImagery |

## Data Collection Methods

EEG data were acquired at 256 Hz using 64 channels (60 EEG, 4 EOG) with a BrainProducts ActiCHamp system. Preprocessing included bandpass filtering (8-70 Hz, 5th order Butterworth), 60 Hz notch filtering, EOG artifact removal via adaptive filtering. Trials were 2 seconds in duration, extracted from a 5-second post-stimulus interval following an auditory beep sequence.

## How to Access via MOABB

Install MOABB and load this dataset directly:

```python
from moabb.datasets import Nguyen2017_S
from moabb.paradigms import MotorImagery
paradigm = MotorImagery()

dataset = Nguyen2017_S()
X, y, metadata = paradigm.get_data(dataset)
```

For more details see the [MOABB documentation](https://moabb.neurotechx.com/) and the
[MOABB dataset page](https://moabb.neurotechx.com/docs/generated/moabb.datasets.Nguyen2017_S.html).

## Citation

If you use this dataset please cite the primary publication:

> DOI: [10.1088/1741-2552/aa8235](https://doi.org/10.1088/1741-2552/aa8235)

## NEMAR / MOABB Benchmark Collection

This BIDS-formatted dataset was converted from the original data using the
[MOABB](https://moabb.neurotechx.com/) pipeline and re-hosted on
[NEMAR](https://nemar.org/) as part of the MOABB benchmark collection.
The original data and license terms apply — see `dataset_description.json` for details.
