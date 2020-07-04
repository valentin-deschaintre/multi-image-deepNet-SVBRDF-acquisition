# Guided Fine-Tuning for Large-Scale Material Transfer
![teaser](https://team.inria.fr/graphdeco/files/2019/06/teaser_v0.jpg)
This repository contains the code for our paper "Flexible SVBRDF Capture with a Multi-Image Deep Network, Valentin Deschaintre, Miika Aittala, Fredo Durand, George Drettakis, Adrien Bousseau. Computer Graphics Forum (Eurographics Symposium on Rendering Conference Proceedings), jul 2019".

The project webpage can be found here: https://team.inria.fr/graphdeco/projects/multi-materials/

**The data for the pre-training can be found on the project webpage.**

## Paper abstract
Empowered by deep learning, recent methods for material capture can estimate a spatially-varying reflectance from a single photograph. Such lightweight capture is in stark contrast with the tens or hundreds of pictures required by traditional optimization-based approaches. However, a single image is often simply not enough to observe the rich appearance of real-world materials. We present a deep-learning method capable of estimating material appearance from a variable number of uncalibrated and unordered pictures captured with a handheld camera and flash. Thanks to an order-independent fusing layer, this architecture extracts the most useful information from each picture, while benefiting from strong priors learned from data. The method can handle both view and light direction variation without calibration. We show how our method improves its prediction with the number of input pictures, and reaches high quality reconstructions with as little as 1 to 10 images — a sweet spot between existing single-image and complex multi-image approaches.

## Software requirements
This code relies on Tensorflow 1.X but can be adapted to TF 2.X with the following compatibility code:

It is based on python 3.X, numpy, imageio and opencv for python.


## Re-training the network
To retrain the network, the basic version is to run trainNetwork.sh
You can find the training dataset (1.3Go) here: https://repo-sam.inria.fr/fungraph/multi_image_materials/supplemental_multi_images/materialsData_multi_image.zip
(A higher definition version of this dataset is available in our more recent project repository: https://github.com/valentin-deschaintre/Guided_fine_tuning_SVBRDF)

## Running the network inference
**First download the trained weights here: https://repo-sam.inria.fr/fungraph/multi_image_materials/supplemental_multi_images/checkpointTrained.zip**

You can then run testModel.sh

To achieve the best results, one of the inputs should have an approximately centered flash image.

## Bibtex
If you use our code, please cite our paper:

@Article{DADDB19,
  author       = "Deschaintre, Valentin and Aittala, Miika and Durand, Fr\'edo and Drettakis, George and Bousseau, Adrien",
  title        = "Flexible SVBRDF Capture with a Multi-Image Deep Network",
  journal      = "Computer Graphics Forum (Proceedings of the Eurographics Symposium on Rendering)",
  number       = "4",
  volume       = "38",
  month        = "July",
  year         = "2019",
  keywords     = "Reflectance modeling, Image processing, Material capture, Appearance capture, SVBRDF, Deep learning",
  url          = "http://www-sop.inria.fr/reves/Basilic/2019/DADDB19"
}


