# LE-GAN-Layout-enhanced-Adversarial-Network-for-Text-to-Image-Synthesis- Under Review

### Introduction


**Arxiv:** 

### How to use

**Python**

- Python2.7
- Pytorch0.4 (`conda install pytorch=0.4.1 cuda90 torchvision=0.2.1 -c pytorch`)
- tensorflow (`pip install --ignore-installed --upgrade https://storage.googleapis.com/tensorflow/linux/gpu/tensorflow_gpu-1.12.0-cp27-none-linux_x86_64.whl`)
- `pip install easydict pathlib`
- `conda install requests nltk pandas scikit-image pyyaml cudatoolkit=9.0`


**Data**
1. Download metadata for [birds](https://drive.google.com/open?id=1O_LtUP9sch09QH3s_EBAgLEctBQ5JBSJ) [coco](https://drive.google.com/open?id=1rSnbIGNDGZeHlsUlLdahj0RJ9oo6lgH9) and save them to `data/`
    - `python google_drive.py 1O_LtUP9sch09QH3s_EBAgLEctBQ5JBSJ ./data/bird.zip`
    - `python google_drive.py 1rSnbIGNDGZeHlsUlLdahj0RJ9oo6lgH9 ./data/coco.zip`

2. Download the [birds](http://www.vision.caltech.edu/visipedia/CUB-200-2011.html) image data. Extract them to `data/birds/`
    - `cd data/birds`
    - `wget http://www.vision.caltech.edu/visipedia-data/CUB-200-2011/CUB_200_2011.tgz`
    - `tar -xvzf CUB_200_2011.tgz`
    
3. Download [coco](http://cocodataset.org/#download) dataset and extract the images to `data/coco/`
    - `cd data/coco`
    - `wget http://images.cocodataset.org/zips/train2014.zip`
    - `wget http://images.cocodataset.org/zips/val2014.zip`
    - `unzip train2014.zip`
    - `unzip val2014.zip`
    - `mv train2014 images`
    - `cp val2014/* images`

**Pretrained Models**
LE-GAN for bird. Download and save it to models https://pan.baidu.com/s/1EhCc4Hz16b0MgIq1fV4O4Q PASSWD：XIUP

LE-GAN for coco. Download and save it to models https://pan.baidu.com/s/10bOuC30AlOAX9km4gjGbbA PASSWD：XIUP

**Training**
    - bird: `python main.py --cfg cfg/bird_LEGAN.yml --gpu 0`
    - coco: `python main.py --cfg cfg/coco_LEGAN.yml --gpu 0`

**Validation**
    - `python main.py --cfg cfg/eval_bird.yml --gpu 0`
    - `python main.py --cfg cfg/eval_coco.yml --gpu 0`


### License
This code is released under the MIT License (refer to the LICENSE file for details). 

