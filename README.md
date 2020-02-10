# Overfitting in adversarially robust deep learning

This is supplemental material containing the code and training logs for the paper "Overfitting in adversarially robust deep learning" submitted to ICML 2020. 

The experiments for CIFAR10, CIFAR100, and SVHN are in `train_cifar.py`, `train_cifar100.py`, `train_svhn.py` respectively. 
+ CIFAR10 training with semisupervised data is done in `train_cifar_semisupervised_half.py`, and uses the 500K pseudo-labeled TinyImages data from <https://github.com/yaircarmon/semisup-adv>

For ImageNet training, we used <https://github.com/MadryLab/robustness>. The resulting logged data is stored in `.pth` which can be loaded with `torch.load` and are simply dictionaries of logged data. 

Logs are all located in the `experiments` folder, and each subfolder corresponds to a set of experiments carried in the paper. 

Model weights for the preactivation ResNet18 trained with validation based early stopping, as well as the WideResNets trained in this paper, can be found at <https://drive.google.com/open?id=1xslETwg3nl_Mwaq_kbZiZVo9BnhCcVMG>
