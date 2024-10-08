_Qule won the first place at the Quantum Science and Technology Hackathon - 2022. Learn more here - [IEEE Quantum - QSTH 2022](https://quantum.ieee.org/education/qsth-2022)_

# Qule
Qule is a quantum enhanced AI driven drug design tool. 
It implements a quantum generator (may be run on AWS Braket) and classical discriminator and a classical reward network. 

This library is built on the following projects.
* [yongqyu/MolGAN-pytorch](https://github.com/yongqyu/MolGAN-pytorch)
* [Jundeli/quantum-gan](https://github.com/jundeli/quantum-gan)

> Attention: The code for this project is not available to view right now. It'll be back up shortly

## Dependencies

* **python>=3.7**
* **pytorch>=0.4.1**: https://pytorch.org
* **rdkit**: https://www.rdkit.org
* **pennylane**
* **tensorflow==1.15**
* **frechetdist**

## Dataset
* run bash script `data/gdb9_generater.sh` to download gdb database and then run `data/sparse_molecular_dataset.py` to generate molecular graph dataset used to train the model.

## Training
```
python main.py --mode=train

```


## Prediction
To run the model against test dataset, make sure the model is fully trainned in the first place.
```
python main.py --mode=test
```
## Structure
`main.py` parses the command line arguments and pass it to the `Qgans_molGen.py` which accesses generator and discriminator model from `models.py` which in turn accesses `layers.py` and `utils.py` to evaluate the molecule generated.  



Contributers:
Padmapriya Mohan, Sabarikirishwaran Ponnambalam, Tarush Singh, Sphoorthy Nadimpalli, Shubhang Mathur



