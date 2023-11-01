# 1DMT
SyntheticMT1D.ipynb is the basic, step-by-step code to generate synthetic 1D resisitivity-depth models in a similar manner to Wu's 2023 paper on Fast Bayesian Inversion of AEM data. This code also generates synthetic 1D MT data using SimPEG.

SyntheticDataset1D.ipynb follows the same algorithm as SyntheticMT1D, but generates 162,000 samples to be used as training data for the neural network and normalizing flows inversion methods. This code filters out samples in which the shallow portion of the interpolated resistivity-depth model overshoots geologically realistic resistivity bounds (<10-1 and >10^4 Ohm m). Training and target datasets are saved as pytorch tensors and .txt files.

1DMT_NN_Inversion.ipynb is a basic feed-forward neural network to invert the synthetic MT data from SyntheticDataset1D into the interpolated resisitivity-depth models.
