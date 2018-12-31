# fast-tsetlin-machine-with-mnist-demo
An implementation of the Tsetlin Machine (https://arxiv.org/abs/1804.01508) using bitwise operations for increased learning- and classification speed.

On the MNIST dataset, the bit manipulation leads to approx.
* 10 times smaller memory footprint,
* 8 times quicker classification, and
* 3.5 times faster learning,

compared to the vanilla C implementation (https://github.com/cair/TsetlinMachineC). 

# MNIST Demo
```bash
make
./MNISTDemoBits 

EPOCH 1
Training Time: 178.6 s
Evaluation Time: 13.4 s
Accuracy Dataset I: 94.8
Accuracy Dataset II: 95.2

EPOCH 2
Training Time: 130.8 s
Evaluation Time: 15.4 s
Accuracy Dataset I: 95.4
Accuracy Dataset II: 95.7

EPOCH 3
Training Time: 121.7 s
Evaluation Time: 16.0 s
Accuracy Dataset I: 96.2
Accuracy Dataset II: 96.7

EPOCH 4
Training Time: 105.7 s
Evaluation Time: 15.6 s
Accuracy Dataset I: 96.5
Accuracy Dataset II: 96.7

EPOCH 5
Training Time: 100.5 s
Evaluation Time: 15.3 s
Accuracy Dataset I: 96.8
Accuracy Dataset II: 97.0
...

EPOCH 246
Training Time: 60.8 s
Evaluation Time: 14.1 s
Accuracy Dataset I: 98.2
Accuracy Dataset II: 98.3

EPOCH 247
Training Time: 61.6 s
Evaluation Time: 14.5 s
Accuracy Dataset I: 98.2
Accuracy Dataset II: 98.4

EPOCH 248
Training Time: 60.1 s
Evaluation Time: 15.4 s
Accuracy Dataset I: 98.3
Accuracy Dataset II: 98.3

EPOCH 249
Training Time: 59.5 s
Evaluation Time: 15.3 s
Accuracy Dataset I: 98.1
Accuracy Dataset II: 98.2

EPOCH 250
Training Time: 61.4 s
Evaluation Time: 16.1 s
Accuracy Dataset I: 98.2
Accuracy Dataset II: 98.2
```
# Data Preparation

Data source: https://github.com/mnielsen/neural-networks-and-deep-learning/tree/master/data, http://yann.lecun.com/exdb/mnist/

# Further Work

* Perform a more extensive hyperparameter search (manipulating THRESHOLD, CLAUSES, S, as well as binarization of MNIST).
* Investigate effect of using an Ensemble of Tsetlin Machines.
