# RandNE
This is a sample implementation of "[Billion-scale Network Embedding with Iterative Random Projection](https://zw-zhang.github.io/files/2018_ICDM_RandNE.pdf)" (ICDM 2018).

We are only able to provide executable main functions for now and apologize for any inconvenience it might bring.

### Requirements
```
MATLAB (MATLAB 2017a works fine for me)
```

### Usage
##### Example Usage
```
See Sample_Run.m for a sample run on the BlogCatalog network
```
##### Functions
```
Sample_Run.m: a sample run on the BlogCatalog network, see annotations for detail
RandNE_Projection.p: calculate projection results of different orders by performing iterative random projection
    Inputs: sparse adjacency matrix, order q, dimension d, whether use orthogonal projection, random seed
    Outputs:  a cell containing decomposed parts U_0 ... U_q
RandNE_Combine.p: combine different orders with given weights
    Inputs: a list of decomposed parts generated by RandNE_Projection, a vector of weights for each order w_0 ... w_q
    Outputs: final embedding vectors U
RandNE_Update.p: update embeddings for dynamic networks
    Inputs:  original adjacency matrix, the changes of adjacency matrix, original decomposed parts
    Outputs: updated decomposed parts
GS.p: perform Gram–Schmidt process to obtain orthogonal projections

```
### Cite
If you find this code useful, please cite our paper:
```
@inproceedings{zhang2018billion,
  title={Billion-scale Network Embedding with Iterative Random Projection},
  author={Zhang, Ziwei and Cui, Peng and Li, Haoyang and Wang, Xiao and Zhu, Wenwu},
  booktitle={Data Mining (ICDM), 2018 IEEE International Conference on},
  year={2018},
  organization={IEEE}
}
```