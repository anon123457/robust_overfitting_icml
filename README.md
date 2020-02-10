# Overfitting in adversarially robust deep learning

This is supplemental material containing the code and training logs for the paper "Overfitting in adversarially robust deep learning" submitted to ICML 2020. 

The experiments for CIFAR10, CIFAR100, and SVHN are in `train_cifar.py`, `train_cifar100.py`, `train_svhn.py` respectively. 
+ CIFAR10 training with semisupervised data is done in `train_cifar_semisupervised_half.py`, and uses the 500K pseudo-labeled TinyImages data from <https://github.com/yaircarmon/semisup-adv>
+ TRADES training is done with the repository located at <https://github.com/yaodongyu/TRADES>, with the only modification being the changes to the learning rate schedule to train to convergence (to decay at epochs 100 and 150 out of 200 total epochs). 

For ImageNet training, we used the repository located at <https://github.com/MadryLab/robustness> with no modifications. The resulting logged data is stored in `.pth` which can be loaded with `torch.load` and are simply dictionaries of logged data. 

Logs are all located in the `experiments` folder, and each subfolder corresponds to a set of experiments carried in the paper. 

Model weights for the following models can be found at <https://drive.google.com/open?id=1xslETwg3nl_Mwaq_kbZiZVo9BnhCcVMG>
+ The best checkpoints for CIFAR10 WideResNets for width factor 10 and 20 (from the double descent curve)
+ The best checkpoints for SVHN/CIFAR10/CIFAR100/ImageNet models reported in Table 1 (the ImageNet models are in the format used by <https://github.com/MadryLab/robustness>)
