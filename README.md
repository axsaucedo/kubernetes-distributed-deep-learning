
# PaddlePaddle Kubernetes Image Recognition

This repository contains an implementation of the demo for [Paddlepaddle](https://github.com/PaddlePaddle/Paddle) - Badiu's Parallel Distributed Deep Learning framework, which runs with [Kubernetes](https://github.com/kubernetes/kubernetes).

The code in this repo trains a model using the CFAR-10 images in a distributed kubernetes system. 

## Why this is awesome

Deep learning requires an insane load to process huge amounts of data, which makes it insanely complex for DevOps teams to develop complex architectures that can keep up with the requirements.

Baidu open sourced their framwework that works on top of kubernetes to make life much easier to DevOps teams in AI projects.

## About Kubernetes

There are loads of awesome resources about Kubernetes, but if you want to get a quikc overview of what it does and why it's awesome I recommend you to check out this [short set of videos introducing its capabilities](https://www.youtube.com/watch?v=S6CVIqQeJww&list=PLj_IGCS9P2SkmHxS8-i24azCIGEneJQrA)

# #LetsDoThis

### Run environment

If you want to be able to edit / view the files in your host file, clone this server, and run the Paddlepaddle Docker Image whilst mounting this repo folder:

``` bash
docker run -ti -v /path/to/this/repo:/folder/in/your/container [PPIMAGE] /bin/bash
```

### Install Dependencies
In order to run this, you need to install image, but before make sure you install all the required dependencies:

``` bash
sudo apt-get install libjpeg-dev
pip install pillow
```

### Download
You need to first download the data:

``` bash
cd demo/image_classification/data/
sh download_cifar.sh
```

### Preprocess the images

``` bash 
cd demo/image_classification/
sh preprocess.sh
```

### Predict 

``` bash
./predict.sh
```


Credits go to the [PaddlePaddle Baidu](https://github.com/PaddlePaddle/Paddle) team for open sourcing such an awesome framework! Check out their repo, and do submit any issues you find!