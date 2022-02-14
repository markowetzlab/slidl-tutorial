Learning SliDL, a Python library of pre- and post-processing tools for applying deep learning to whole-slide images
=====
[SliDL](https://github.com/markowetzlab/slidml) is a Python library for performing deep learning image analysis on whole-slide images (WSIs), including deep tissue, artefact, and background filtering, tile extraction, model inference, model evaluation and more. This repository serves to teach users how to apply `SliDL` on both a classification and a segmentation example problem from start to finish using best practices.

<p align="center">
  <img src="https://raw.githubusercontent.com/markowetzlab/slidl/main/docs/source/_static/figure1.png" width="700" />
</p>

Installing SliDL and its depedencies
----
`SliDL` can also be installed via the Python Package Index (PyPI):
```
pip install slidl
```

Running the SliDL tutorial
----
First clone this repository:
```
git clone https://github.com/markowetzlab/slidl-tutorial
```
The tutorial uses an example subset lymph node WSIs from the [CAMELYON16 challenge](https://camelyon16.grand-challenge.org/). Some of these WSIs contain breast cancer metastases and the goal of the tutorial is to use SliDL to train deep learning models to identify metastasis-containing slides and slide regions, and then to evaluate the performance of those models.

Create a directory called `wsi_data` where there is at least 38 GB of disk space. Download the following 18 WSIs from the [CAMELYON16 dataset](https://drive.google.com/drive/folders/0BzsdkU4jWx9Ba2x1NTZhdzQ5Zjg?resourcekey=0-g2TRih6YKi5P2O1SiBB1LA) into `wsi_data`:

* `normal/normal_001.tif`
* `normal/normal_010.tif`
* `normal/normal_028.tif`
* `normal/normal_037.tif`
* `normal/normal_055.tif`
* `normal/normal_074.tif`
* `normal/normal_111.tif`
* `normal/normal_141.tif`
* `normal/normal_160.tif`
* `tumor/tumor_009.tif`
* `tumor/tumor_011.tif`
* `tumor/tumor_036.tif`
* `tumor/tumor_039.tif`
* `tumor/tumor_044.tif`
* `tumor/tumor_046.tif`
* `tumor/tumor_058.tif`
* `tumor/tumor_076.tif`
* `tumor/tumor_085.tif`

Install Jupyter notebook into `slidl-env`:
```
conda install -c conda-forge notebook
```
Now that the requisite software and data have been downloaded, you are ready to begin the tutorial, which is contained in the Jupyter notebook `slidl-tutorial.ipynb` in this repository. Start notebook and then navigate to that document in the interface:
```
jupyter notebook
```
Once up and running, `slidl-tutorial.ipynb` contains instructions for running the tutorial. For instructions on running Jupyter notebooks, see the [Jupyter documentation](https://jupyter.org/documentation).

The results of a completed tutorial run can be found [here](https://doi.org/10.5281/zenodo.5006409).

The implementation of the [U-Net segmentation architecture](https://arxiv.org/abs/1505.04597) contained in this repository and some related segmentation code comes from [milesial's](https://github.com/milesial) [open source project](https://github.com/milesial/Pytorch-UNet).

Documentation
----
The complete documentation for `SliDL` including its API reference can be found [here](https://slidl.readthedocs.io/).

Disclaimer
----
Note that this is prerelease software. Please use accordingly.
