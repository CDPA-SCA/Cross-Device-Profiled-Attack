# Cross-Device-Profiled-Attack
 
This repository contains Demos and data on how to reproduce the results presented in "Cross-Device Profiled Side-Channel Attack with Unsupervised Domain Adaptation."

## Datasets

### Different_Devices

1. **XMEGA**. Unprotected software AES-128 implementation. Side-channel traces are acquired from eight XMEGA chips. The secret keys (first byte) for the eight devices are set to 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07, 0x08.
2. **XMEGA_masked**. Simulated masking scheme implemented by LD and ST assembly instructions. Side-channel traces are acquired from eight XMEGA chips. The secret keys (first byte) for the eight devices are set to 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07, 0x08.
3. **SAKURA_AES**. Unprotected hardware AES-128 implementation. Side-channel traces are acquired from three SAKURA-G boards. The last round keys (second byte) for the three devices are 0x21, 0xCD, and 0x8F.
4. **CHES_CTF_2018**. Masked software AES-128 implementation. We use the dataset provided by Perin et al. The secret keys  (first byte) for the profiling and target devices are 0x17 and 0x2E. This dataset is available at [https://github.com/AISyLab/EnsembleSCA](https://github.com/AISyLab/EnsembleSCA).

### Different_Implementations
We simulate different implementations by adding artificial countermeasures/noise to the original [ASCAD](https://github.com/ANSSI-FR/ASCAD "ASCAD") dataset. These experiments simulate a complex attack scenario that the target device is treated as a black box that can turn on side-channel countermeasures. The added countermeasures/noise include:
1. **Gaussian Noise**.
2. **Desynchronization**.
3. **Clock Jitters**.
### Different_Probe_Positions
1. **XMEAGA_EM**. Unprotected AES-128 encryption. This dataset is captured using a near-field probe, each time at a similar position but with human error. The secret keys (first byte) for the eight devices are set to 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07, 0x08.


----------

## Repository structure

Each dataset is composed of the following folders and script:

- **./Data:** the dataset (.npy format) used in the experiments. 
- **./models**: contains the pre-trained model, fine-tuned model, etc.
- **..._CDPA_Demo.ipynb**: the notebook file that contains both codes and outputs. This notebook demonstrates how to load a dataset, how to pre-process the data, how to fine-tune a network, how to evaluate the pre-trained and fine-tuned models, etc. 


