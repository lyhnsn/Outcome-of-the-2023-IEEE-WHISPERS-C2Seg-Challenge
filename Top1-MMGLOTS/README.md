# Top1 Solution: MMGLOTS: Multi-modal Global-local Transformer Segmentor For Remote Sensing Image Segmentation.
The codebase of Top1 Solution: MMGLOTS: Multi-modal Global-local Transformer Segmentor For Remote Sensing Image Segmentation.

## Installation

Please refer to [get_started.md](https://github.com/open-mmlab/mmsegmentation/blob/main/docs/en/get_started.md#installation) for installation and [dataset_prepare.md](https://github.com/open-mmlab/mmsegmentation/blob/main/docs/en/user_guides/2_dataset_prepare.md#prepare-datasets) for dataset preparation.

## Pre-trained Model

Download the [Model](https://drive.google.com/file/d/1yV070cXTrkCN2FTHKM2DIXI_dtVjaTJ6/view?usp=sharing) and put it under the folder 'pretrain'.

## Data Preparation

Put the remote sensing datasets into `data/` directory as follows:

data format:
```
    ├── data
    │   ├── c2seg_ab
    │   │   ├── img_dir
    │   │   │   ├── train
    │   │   │   │   ├── msi
    │   │   │   │   │   ├── xxx.tiff
    │   │   │   │   │   ├── yyy.tiff
    │   │   │   │   │   ├── zzz.tiff
    │   │   │   │   ├── hsi
    │   │   │   │   │   ├── xxx.tiff
    │   │   │   │   ├── sar
    │   │   │   │   │   ├── xxx.tiff
    │   │   │   ├── val
    │   │   │   │
    │   │   ├── ann_dir
    │   │   │   ├── train
    │   │   │   │   ├── xxx.tiff
    │   │   │   │   ├── yyy.tiff
    │   │   │   │   ├── zzz.tiff
    │   │   │   │   │
    │   │   │   ├── val
```

## Usage

### train (example)

`python tools/train.py configs/mmglots/mmglots-base_640x640_160k_ab.py --gpu-id 0`

denotes "train MMGLOTS on c2seg-ab dataset on gpu 0".

### test (example)

`python tools/test.py configs/mmglots/mmglots-base_640x640_160k_ab.py work_dirs/mmglots-base_640x640_160k_ab/lastest.pth --eval mIoU`

denotes "test the latest trained model of MMGLOTS on gpu 0".

## Reference

[MMSegmentation](https://github.com/open-mmlab/mmsegmentation/tree/main)

[BeiT](https://github.com/microsoft/unilm/tree/master/beit2)
