# Convolutional Neural Networks (CNN)

`CNN_For_CIFAR10.ipynb` trains a three-block convolutional network for ten-class CIFAR-10 image classification using PyTorch and torchvision. It uses CUDA when available and otherwise runs on the CPU.

Install the root requirements and run the notebook from this folder. CIFAR-10 downloads automatically into `./data` on the first run. This generated dataset folder is excluded from the repository. The notebook trains for ten epochs and reports test accuracy.
