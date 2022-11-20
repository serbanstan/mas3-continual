# Code for ["Unsupervised Model Adaptation for Continual Semantic Segmentation"](https://arxiv.org/abs/2009.12518)
The code was tested using Tensorflow 2.2 and CUDA 11.2, with driver version 460.xx. 

If you find our codebase useful in your work, please cite our paper at
```
@inproceedings{stan2021unsupervised,
  title={Unsupervised model adaptation for continual semantic segmentation},
  author={Stan, Serban and Rostami, Mohammad},
  booktitle={Proceedings of the AAAI Conference on Artificial Intelligence},
  volume={35},
  number={3},
  pages={2593--2601},
  year={2021}
}
```

## Data

The **data** directory (only containing file paths) is meant to store the original versions of the [GTA5](https://download.visinf.tu-darmstadt.de/data/from_games/), 
[SYNTHIA-RAND-CITYSCAPES](http://synthia-dataset.net/) and [CITYSCAPES](https://www.cityscapes-dataset.com/) datasets. These datasets are available online, and are not included in this repository.

## Running the code

The datasets need to be prepared before running the E2E model. This is done via the **process_gta5_cityscapes.ipynb** or **process_synthia_cityscapes.ipynb**
notebooks. The processed images will be available in the **processed-data** folder.

After loading the data and processing it, running E2E training and adaptation can be done by running
**vgg16-deeplabv3-GTA5-CITYSCAPES.ipynb** or **vgg16-deeplabv3-SYNTHIA-CITYSCAPES.ipynb**

The notebooks will save model weights in the **weights** folder. Currently, this folder comes prepopulated with weights corresponding 
to the runs present in the notebooks. 

