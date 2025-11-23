This repository is a simplified version to understand and experiment with the code from [UnchartedRLab/QSeer](https://github.com/UnchartedRLab/QSeer)  
based on the paper: [QSeer Paper](https://arxiv.org/abs/2505.06810).

---

## Setup

1. **Create and activate conda environment**
```bash
conda create -n qseer python=3.10 -y
conda activate qseer
````

2. **Install dependencies**

```bash
pip install -r requirements.txt
```

---

## Prepare Data

1. **Download data** from [QSeer data repository](https://github.com/UnchartedRLab/QSeer).

2. **Extract data**

   * Make sure you have `7z` installed.
   * Command to extract:

```bash
sudo apt update
sudo apt install p7zip-full -y
7z x data/data.7z -odata/
```

* This will put all `.pkl` files into the `data/` directory.

---

## Run QSeer

1. Open and follow the steps in `qseer.ipynb`.

2. **Modifications for smaller tests or GPU**

   * To use NumPy backend instead of default:

```python
K = tc.set_backend("numpy")
```

* You can also modify the notebook to train/test on a smaller sample instead of the full dataset for faster experimentation.

---

## Notes

* This repo is intended for **learning and experimentation** with QSeer.
* Any modifications were made to **fit GPU memory constraints** or simplify testing.
