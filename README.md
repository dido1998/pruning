# pruning
This repo is demonstrates pruning in tensorflow.

We explore two kinds of pruning: weight pruning and unit pruning. We show that upto 80-90% of the weights can be pruned without any significant loss in accuracy. We can also utilize this sparsity to speed up inference. 

Weight Pruning: set individual weights in the weight matrix to zero. This corresponds to deleting connections as in the figure above. Here, to achieve sparsity of k% we rank the individual weights in weight matrix W according to their magnitude (absolute value) |wi,j|, and then set to zero the smallest k%.

Unit Pruning: set entire columns to zero in the weight matrix to zero, in effect deleting the corresponding output neuron.
Here to achieve sparsity of k% we rank the the columns of a weight matrix according to their L2-norm and delete the smallest k%.
 
## Requirements
```
Tensorflow 1.12.0
seaborn 0.9.0
matplotlib 3.0.2
pandas 0.23.4 
numpy 1.15.4
tqdm 4.29.0
```


