

## Requirments
* python 3.7
* pytorch 1.4.0 
* torchvision 0.5.0
* numpy
* PIL
* h5py
* tqdm
* tensorboard
* Prefetch version of DataLoader: https://github.com/IgorSusmelj/pytorch-styleguide/issues/5
* nlgeval*: https://github.com/Maluuba/nlg-eval



## Pre-preprocess

1. `mkdir ./data` and place [Visual Genome Dataset](http://visualgenome.org/) in a sub directory `visual-genome`
    * Images are in two directories `./data/visual-genome/VG_100K` and `./data/visual-genome/VG_100K_2`
    * Annotation files are `./data/visual-genome/region_descriptions.json` and `./data/visual-genome/image_data.json`
2. `python preprocess.py`
3. Now we get `./data/VG-regions-dicts-lite.pkl` and `./data/VG-regions-lite.h5`. See preprocess.py for more details.
4. After preprocessing, file structures are listed below:
```
    data
    ├── visual-genome
    │   ├── VG_100K
    │   ├── VG_100K_2
    │   ├── region_descriptions.json
    │   └── image_data.json
    ├── VG-regions-dicts-lite.pkl
    └── VG-regions-lite.h5
```


## Start Training

1. `mkdir model_params`
2. `python train.py`
3. change settings by `set_args()` and global variables

